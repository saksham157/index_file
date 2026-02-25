pipeline {
    agent any

    stages {
        stage('Deploy to Apache') {
            steps {
                sh '''
                sudo cp index.html /var/www/html/
                sudo systemctl restart apache2
                '''
            }
        }
    }
}
