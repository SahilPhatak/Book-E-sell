pipeline {
    agent any

    stages {
        stage('install pkgs') {
            steps { 
                 sh '''
                echo "Installing nginx application"
                sudo apt-get install nginx -y
            '''
            }
        }
        stage('configure appln') {
            steps {
                 sh '''
                echo "This is Test stage"
                systemctl start nginx
                systemctl enable nginx
            '''
            }
        }
        stage('web-page') {
            steps {
                echo "This is webpage stage"
                sh 'sudo cp /home/ubuntu/2095_level/ /var/www/html'
            }
        }
        stage('deployment') {
            steps {
                echo "This is Deployment stage"
        }

    }
}
