pipeline {
    agent {
        node{
            label 'maven'
        }
        
    }

    stages {
        stage('clone code') {
            steps {
               git branch: 'main', url: 'https://github.com/saad-react/ValaxyProj.git'
            }
        }
    }

    enviroment{
        PATH = "/opt/apache-maven-3.9.6/bin:$PATH"
    }

    stages {
        stage('build') {
            steps {
               sh 'mvn clean package'
            }
        }
    }
}
