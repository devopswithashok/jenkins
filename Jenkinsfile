pipeline{
    agent any 
    stages{
        stage("Build job"){
            steps{
                echo "========Build Done========"
            }
            
        }
        stage("Test Job"){
            steps{
                echo "========Test Done========"
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