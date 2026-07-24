pipeline {
    agent { label "python" }

    triggers {
        pollSCM('H/3 * * * *')
    }

    environment {
        APP = "Inventory"
        ENV = "Development"
    }

    stages {

        stage('Welcome') {
            steps {
                script {
                    def app = "Inventory"
                    def version = "1.0"
                    echo version
                    echo app
                    echo ENV
                }

                echo "Welcome to Jenkins Pipeline"
            }
        }

        stage('Execute Linux Commands') {
            steps {
                sh "pwd"
                sh "hostname"
                sh "whoami"
                sh "date"
            }
        }

       stage('Built-in Jenkins Variables') {
       steps{
        echo "BUILD_NUMBER = ${BUILD_NUMBER}"
                echo "JOB_NAME = ${JOB_NAME}"
                echo "NODE_NAME = ${NODE_NAME}"
                echo "WORKSPACE = ${WORKSPACE}"
                echo "BUILD_ID = ${BUILD_ID}"
            } 

       }

       stage('String Interpolation') {
            steps {
                script {
                    def app = "Inventory"
                    def version = "1.0"
                    echo "Building ${app} Version ${version}"
                }
            }

    }
}