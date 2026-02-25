stage('Deploy to Apache') {
    steps {
        sh '''
        set -xe

        echo "===== WORKSPACE FILE ====="
        pwd
        ls -l
        echo "First lines of workspace index:"
        head -n 5 index.html || true

        echo "===== COPYING ====="
        sudo install -m 644 index.html /var/www/html/index.html

        echo "===== APACHE FILE ====="
        sudo ls -l /var/www/html/index.html
        echo "First lines of apache index:"
        sudo head -n 5 /var/www/html/index.html

        echo "===== RELOAD ====="
        sudo systemctl reload apache2
        '''
    }
}
