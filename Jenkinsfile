pipeline {
    agent {
        docker {
            image 'maven:3.6-alpine' 
            args '-u root -v /home/jenkins/mvnrepo:/root/.m2'
        }
    }
    stages {
        stage('Pull Git Demo') {
            steps{
                git 'https://github.com/niufuwang/springboot-demo1.git'
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
