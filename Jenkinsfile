pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/yourusername/your-repo.git'
            }
        }

        stage('Deploy to Apache2 Server') {
            steps {
                sh '''
                echo "Copying Index.html to remote Apache2 server"
                scp -o StrictHostKeyChecking=no -i /var/lib/jenkins/.ssh/id_rsa Index.html ubuntu@15.206.88.161:/var/www/html/
                '''
            }
        }
    }
}
