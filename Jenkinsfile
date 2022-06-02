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
               sh 'cd odoo  && docker build -t mybuildimage .'
            }
        }
    
     
        stage('images') {
            steps {
               sh '  docker images'
            }
        }
    }
}

