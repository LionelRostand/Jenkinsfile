pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
               sh 'ssh -oStrictHostKeyChecking=no root@192.168.1.20 git clone https://github.com/LionelRostand/odoo.git'
            }
        }
    
     
        stage('Built') {
            steps {
               sh 'ssh -oStrictHostKeyChecking=no root@192.168.1.20  cd odoo  && docker build -t mybuildimage .'
            }
        }
    
     
        stage('images') {
            steps {
               sh 'ssh -oStrictHostKeyChecking=no root@192.168.1.20  docker images'
            }
        }
    }
}

