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
                sh "rm -rf /var/www/html/*.html"
                sh "cp -r /var/www/html"
                sh "systemctl restart nginx"
            }
        }
    }
}
