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
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}