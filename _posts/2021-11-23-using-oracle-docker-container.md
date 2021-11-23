---
layout: post
title: Using Oracle in a Docker Container
description: In this tutorial, I show how you can run a Oracle database in a Docker container
categories:
  - oracle
  - docker
---

Think of a Docker container as a lightweight virtual machine.

By using a text file named Dockerfile, you can describe everything this lightweight virtual machine should contain.

From this Dockerfile, you can build what is called an image. And from that image, instantiate or run one or more containers.

Oracle provides a [GitHub repository](https://github.com/oracle/docker-images) that contains configurations, images, and Dockerfiles for Oracle products.

There are [Dockerfiles for most versions of Oracle database](https://github.com/oracle/docker-images/tree/main/OracleDatabase/SingleInstance/dockerfiles) and if you're using an Intel Mac ([not ARM support right now](https://github.com/oracle/docker-images/blob/main/OracleDatabase/SingleInstance/FAQ.md#can-i-run-oracle-database-containers-on-apple-m1-arm-devices)) or Linux, this repo also offers a script for building a Docker image with any version of Oracle database.

So, assumming you have [Docker installed](https://docs.docker.com/get-docker/), start by cloning the repo (or download it as a ZIP file):
<pre><code class="language-bash">git clone https://github.com/oracle/docker-images</code></pre>


It's a big repository, so if you have Git version 2.22 or above, you can use [sparse checkout](https://www.git-scm.com/docs/git-sparse-checkout) to only download the directory that contains the files for Oracle database:
<pre><code class="language-bash">#1. Check if you have Git 2.22 or above, otherwise update it first
git --version

#2. Clone the empty repo
git clone --no-checkout https://github.com/oracle/docker-images

#3. Cd into the empty repo
cd docker-images

#4. Update the config file to enable sparse checkout
git config core.sparseCheckout true

#5. Initialize sparse-checkout
git sparse-checkout init --cone

#6. Checkout the Oracle database directory
git sparse-checkout set OracleDatabase/SingleInstance
</code></pre>

In any case, the next thing you have to do is decide what version of the Oracle database you want to use and download the corresponding Linux installation ZIP file from the [official Oracle download page](http://www.oracle.com/technetwork/database/enterprise-edition/downloads/index.html).

![Linux installation ZIP file]({{ site.url }}/images/2021-11-21-using-oracle-docker-container/01.png)

Once you've downloaded the file, move it to the directory of the corresponding dockerfile (don't unzip it). For example, if you downloaded the installation file for Oracle 19.3, put the installation file in the directory `dockerfiles/19.3.0/`:

![Place installation file in the corresponding dockerfile directory]({{ site.url }}/images/2021-11-21-using-oracle-docker-container/02.png)

Now run the `buildContainerImage.sh` script with the `-h` flag to see all the options you can use to build the Docker image:
<pre><code class="language-bash">./buildContainerImage.sh -h</code></pre>

For example, to build an image for Oracle 19.3 standard edition run the following command:
<pre><code class="language-bash">./buildContainerImage.sh -v 19.3.0 -s </code></pre>

By default, the script builds a slim image, without components needed for patching extension support. If you don't want this, use the build argument `SLIMMING=false` with the `-o` flag:
<pre><code class="language-bash">./buildContainerImage.sh -v 19.3.0 -s -o '--build-arg SLIMMING=false'</code></pre>

The script will create an image of around 3-5 GB and it'll take more than 10 minutes to finish.

After that, you can check the image in your local Docker repository with the command:
<pre><code class="language-bash">docker images</code></pre>


[WORK IN PROGRESS]

