pipeline {
    agent any
    stages{
        stage('vcs') {
            steps {
                git branch: 'dev', url: 'https://github.com/AnasAnsar1/saleor-dashboard.git'
            }
        }
        stage('Image_build_and_Push') {
            steps {
                sh 'docker image build -t anasansarii/saleor-dashboard:jnkdev'
                sh 'docker image push anasansarii/saleor-dashboard:jnkdev'
            }
        }
    }
}