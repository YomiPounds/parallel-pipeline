pipeline{
    agent any 
    stages{
        stage('chkout'){
            steps{
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkinsgit', url: 'https://github.com/YomiPounds/parallel-pipeline.git']]])
            }
        }
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
                echo "I am now a big big boy"
            }
        }
    }
}