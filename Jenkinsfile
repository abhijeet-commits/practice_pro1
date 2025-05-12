pipeline {
    agent any
    stages{
        stage('build project'){
            steps{
                git url:'https://github.com/abhijeet-commits/practice_pro1/', branch: "master"
                sh 'mvn clean package'
              
            }
        }
        stage('Build docker image'){
            steps{
                script{
                    sh 'docker build -t abhisDockerhub/staragileprojectfinance:v1 .'
                    sh 'docker images'
                }
            }
        }
         
        
     stage('Deploy') {
            steps {
                sh 'sudo docker run -itd --name My-first-containe21211 -p 8083:8081 abhisDockerhub/staragileprojectfinance:v1'
                  
                }
            }
        
    }
}
