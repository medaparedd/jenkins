pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
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
                echo "deploying"
            }
        }
    }
}