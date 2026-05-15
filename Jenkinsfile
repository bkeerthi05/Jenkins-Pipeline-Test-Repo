pipeline
{
    agent any
    stages
    {
        stage('checkout'){
            steps{
                git branch : 'main', url : 'https://github.com/bkeerthi05/Jenkins-Pipeline-Test-Repo.git'
            }
        }
        stage('docker version'){
            steps{
                sh 'docker --version'
            }
        }
        stage('docker build'){
            steps{
                sh 'docker build -t nginx:1 .'
                sh 'docker images'
            }
        }
        stage('docker container'){
            steps{
                sh 'docker run -d -p 8001:80 nginx:1'
                sh 'docker ps'
            }
        }
    }
}
