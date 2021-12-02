pipeline{
    agent any

    stages{
        stage("build"){
            steps{
                echo "========executing build========"
            }
        }
        stage("deploy"){
            steps{
                echo "========executing deploy========"
            }
        }
        stage("test"){
            when{
                expression{
                    BRANCH_NAME == 'develop'
                }
            }
            steps{
                echo "========executing test========"
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}

/*
To start a jenkins server with docker
run:
docker run \
  --name jenkins-blueocean \
  --rm \
  --detach \
  --network jenkins \
  --env DOCKER_HOST=tcp://docker:2376 \
  --env DOCKER_CERT_PATH=/certs/client \
  --env DOCKER_TLS_VERIFY=1 \
  --publish 8080:8080 \
  --publish 50000:50000 \
  --volume jenkins-data:/var/jenkins_home \
  --volume jenkins-docker-certs:/certs/client:ro \
  balgaly/myjenkins:1.2  
*/