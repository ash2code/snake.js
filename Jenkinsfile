pipeline {
    agent any

    stages {
        stage("checkout") {
            steps {
                 git branch: 'master', 
                 url: 'https://github.com/ash2code/snake.js.git'
            }
        }
        stage("deploy") {
            steps{
                sh "sudo -S rm -rf /var/www/html/*.html"
                sh "sudo -S cp -r /var/www/html"
                sh "sudo -S systemctl restart nginx"
            }
        }
    }
}
