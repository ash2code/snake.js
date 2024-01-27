pipeline {
    agent none

    stages {
        stage("checkout") {
            steps {
                 git branch: 'master', 
                 url: 'https://github.com/ash2code/snake.js.git'
            }
        }
        stage("deploy") {
            steps{
                sh "sudo rm -rf /var/www/html/*.html"
                sh "sudo cp -r /var/www/html"
                sh "sudo systemctl restart nginx"
            }
        }
    }
}
