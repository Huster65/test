pipeline{
        agent any
        stages{
                stage('Clone'){
                        steps {
                                git 'https://github.com/Huster65/test.git'
                        }
                }
		 stage('Clone'){
                        steps {
                                withDockerRegistry(credentialsId: 'docker-hub', url: 'https://index.docker.io/v1/') { 
				sh 'sudo docker build -t minhnhatbk65/nodejs-v10 .'
				sh 'sudo docker push -t minhnhatbk65/nodejs-v10 .'
				}
                        }
                }
        }
}
