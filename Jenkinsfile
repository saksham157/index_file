pipeline {
    agent any

    stages {
        stage('Deploy to Apache') {
            steps {
                sh '''
                cd /var/www/html
                sudo rm -f index.html
                sudo cp index.html /var/www/html/
                sudo systemctl restart apache2
                '''
            }
        }
    }
}
