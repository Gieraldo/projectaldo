pipeline {   
    agent any     
         
    stages {
        stage('Ready To Deploy') {
            steps{
                echo "ready"
            }   
        } 
        
        stage('Deployment To Server aldoe2') {
            steps{
                echo "deploy to apache2"
                    sshagent(credentials: ['Apache2']) {
                        sh "cd .."
                            sh "ls"
                                sh "scp -r * root@3.111.35.180:/var/www/html/projectaldo"
                                    //sh "ssh root@3.111.35.31 cd /var/www/html/stroberi && pwd && git pull origin master"
                 }    
            }
        }
        
    } 
}
