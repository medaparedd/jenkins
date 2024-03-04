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

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        
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
        stage('check params') {
            steps {
                sh """
                echo "${BIOGRAPHY}"
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
