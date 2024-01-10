pipeline{
    agent any
    stages{
        stage("Build Project"){
            steps{
                echo "========executing A========"
            }
        }
        stage("Test Project"){
            steps{
                echo "========executing A========"
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