pipeline{
    agent any
    stages {
        stage("Git Pull"){
            steps{
                git branch: 'dev',  
                url: 'https://github.com/gbelot2003/docker-laravel.git'
            }
        }
        stage("Creando Entorno Docker"){
            steps{
                sh "docker build ."
            }
        }
    }
    post{
        always{
            echo "========Done========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}


