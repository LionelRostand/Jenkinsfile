pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                 sh ' hostname'
               sh ' git clone https://github.com/LionelRostand/odoo.git'
            }
        }
    
     
        stage('Built') {
            steps {
                 sh ' hostname'
               sh 'cd odoo  && docker-compose up  .'
            }
        }
     
        stage('images') {
            steps {
                 sh ' hostname'
               sh '  docker images'
            }
        }
       
        stage('conteneur  ') {
            steps {
               sh ' docker ps -a '
            }
        }
    }
}

