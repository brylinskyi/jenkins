pipeline {
    agent any

    environment {
        NODE_VERSION = '22'
    }

    stages {
        stage('Prepare') {
            steps {
                echo "Installing Node.js v${NODE_VERSION}..."
                sh '''
                  curl -fsSL https://deb.nodesource.com/setup_${NODE_VERSION}.x | sudo -E bash -
                  sudo apt-get install -y nodejs
                '''
            }
        }

        stage('Build') {
            steps {
                echo "Simulating build by showing npm version..."
                sh 'npm -v'
            }
        }

        stage('Test') {
            steps {
                echo "Simulating test by displaying JENKINS_URL..."
                sh 'echo $JENKINS_URL'
            }
        }
    }
}

