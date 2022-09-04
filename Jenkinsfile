pipeline{
    agent any 
    stages{
        stage('paralle-job'){
            parallel{
                stage('sub-job1'){
                    steps{
                        echo "I am a Devops Engineer"
                    }
                }
                stage('sub-job2'){
                    steps{
                        echo "I am a senior Devops Engineer"
                    }
                }
            }
        }
        stage('mainjob-2'){
            steps{
                echo "I am now a big boy"
            }
        }
    }
}