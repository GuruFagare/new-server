pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/GuruFagare/new-server.git'
            }
        }

        stage('Deploy to Nginx Server') {
            steps {
                sh '''
                echo "Copying index.html to remote Nginx server"
                scp -o StrictHostKeyChecking=no -i /var/lib/jenkins/.ssh/id_rsa index.html ubuntu@15.206.88.161:/var/www/html/
                '''
            }
        }
    }
}
