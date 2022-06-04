pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
               sh ' git clone https://github.com/LionelRostand/odoo.git'
            }
        }
    
     
        stage('Built') {
            steps {
               sh 'cd odoo  && docker build -t myodoo .'
            }
        }
     
        stage('images') {
            steps {
               sh '  docker images'
            }
        }
       
         stage('instoll database') {
            steps {
               sh 'docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres --name db postgres:13'
            }
        }
        stage('instoll odoo ') {
            steps {
               sh ' docker run -p 8069:8069 --name odoo --link db:db -t myodoo '
            }
        }
    }
}

