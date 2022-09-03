pipeline{
	agent any 
	stages{
		stage('first try'){
			steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkinsgit', url: 'https://github.com/YomiPounds/parallel-pipeline.git']]])
			}
			stage('declare your pipe'){
				parallel{
					stage('build 1'){
						steps{
							sh 'pwd'
							sh 'whoami'
						}
					}
					stage('trying second step'){
						steps{
							echo "we shall get there"
						}
					}
				}
			}

		}
		stage('third stag'){
			steps{
				sh 'lscpu'
			}
		}

	}
}