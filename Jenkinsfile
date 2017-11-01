#!groovy

pipeline {
    agent any

    stages {

        stage('Compile Stage'){

            Steps {
                withMaven(maven: 'Maven 3.3.9'){
                    sh 'mvn clean compile'
                }
            }

        }

        stage('Testing Stage') {
            Steps {
                withMaven(maven: 'Maven 3.3.9'){
                    sh 'mvn clean test'
                }
            }
        }

        stage('Deployment Stage') {
            Steps {
                withMaven(maven: 'Maven 3.3.9'){
                    sh 'mvn deploy'
                }
            }
        }
    }
}