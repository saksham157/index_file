pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/saksham157/index_file.git'
            }
        }

        stage('Deploy to Apache') {
            steps {
                sh '''
                set -e
                echo "Deploying latest code..."

                sudo install -m 644 index.html /var/www/html/index.html
                sudo systemctl reload apache2
                '''
            }
        }
    }
}
