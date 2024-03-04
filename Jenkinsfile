pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }

    environment {
        GREETING = "HELLO AKSHIT"
    }

    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
    }

    stages {
        stage('build') {
         steps {
            echo "building"
         }
      }
        stage('test') {
            steps {
                echo "testing"
            }
        }

        stage('deploy') {
            steps {
                sh """
                
                echo "hi"
                """
            }
        }
    }  
        post { 
         always { 
            echo 'I will always say Hello again!'
         }
         failure { 
            echo 'failed'
         }
         success { 
            echo 'success'
         }
      }
    }
