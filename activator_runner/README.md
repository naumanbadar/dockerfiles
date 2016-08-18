Build docker image

    docker build . -t activator-runner

Create new project. In this case the template used is play-scala

    docker run --rm -v $(pwd):/project -v sbt:/root/.sbt -v ivy2:/root/.ivy2 activator-runner activator new __your_project_name__ play-scala
  
Here `sbt` and `ivy2` are named external volumes

After the project is created add the following docker-compose.yml file and continue from there on with docker-compose.

    version: '2'
    services:
      tester:
        image: activator-runner
        volumes:
          - .:/project
          - sbt:/root/.sbt
          - ivy2:/root/.ivy2
        ports:
          - 9000:9000
        command: activator ~compile
    volumes:
      sbt:
        external: true
          #name: sbt
      ivy2:
        external: true
          # name: ivy2


To start the service that will continuously compile on every change in file, simple run:

    docker-compose up
    
If other commands like test or one-off compile run following to enter bash shell:

    docker-compose run tester bash
    
Above command will not expose ports as per design intention of docker according to documentation but if you need to expose ports in one-off commands using `run` then use flag `--service-ports` as :

    docker-compose run --service-ports tester bash