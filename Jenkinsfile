pipeline {
    agent any

    stages {
        stage('Deploy to Apache') {
            steps {
                sh '''
                sudo rm -f index.html
                sudo cp index.html /var/www/html/
                sudo systemctl restart apache2
                '''
            }
        }
    }
}
