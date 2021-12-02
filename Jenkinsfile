pipeline{
    agent any
    environment{
        NEW_VERSION = '0.1.0'
        SERVER_CREDENTIALS = credentials('credentials test)
    }
    stages{
        stage("build"){
            steps{
                echo "========executing build========"
                echo "building version ${NEW_VERSION}"
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
        stage("deploy"){
            steps{
                echo "========executing deploy========"
                echo "deploying with ${SERVER_CREDENTIALS}
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

run jenkins container 
if you want a fresh start -> 'docker volume rm jenkins_home'
    docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts









*/