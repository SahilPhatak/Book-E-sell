pipeline {
    agent any

    stages {

        stage('install pkgs') {
            steps { 
                sh '''
                    echo "Installing nginx application"
                    sudo apt-get update -y
                    sudo apt-get install nginx -y
                '''
            }
        }

        stage('configure appln') {
            steps {
                sh '''
                    echo "Configuring nginx"
                    sudo systemctl start nginx
                    sudo systemctl enable nginx
                '''
            }
        }

        stage('web-page') {
            steps {
                echo "Copying webpage files"
                sh '''
                    sudo cp -r /home/ubuntu/2095_level/* /var/www/html/
                    sudo systemctl restart nginx
                '''
            }
        }

        stage('deployment') {
            steps {
                echo "This is Deployment stage"
            }
        }
    }
}
