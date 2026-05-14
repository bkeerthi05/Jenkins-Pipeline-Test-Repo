pipeline
{
    agent any
    stages
    {
        stage('checkout'){
            steps{
                git branch : 'main', url : 'git@github.com:bkeerthi05/Jenkins-Pipeline-Test-Repo.git'
            }
        }
        stage('docker version'){
            steps{
                sh 'docker --version'
            }
        }
        stage('docker build'){
            steps{
                sh 'sudo docker build -t nginx:1 .'
                sh 'sudo docker images'
            }
        }
        stage('docker container'){
            steps{
                sh 'sudo docker run -d -p 8001:80 nginx:1'
                sh 'sudo docker ps'
            }
        }
    }
}
