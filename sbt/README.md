# How to start container during development & testing

Create image

    docker build -t sbt_runner .

To make sbt container run faster mount local cache in data container

    docker create -v ~/.sbt:/root/.sbt -v ~/.ivy2:/root/.ivy2 --name sbt_helper busybox

Then start container by linking to data container from root of your project

    docker run --rm -it --volumes-from sbt_helper -v $(pwd):/project sbt_runner /bin/bash