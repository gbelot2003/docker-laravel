pipeline{
    agent any
    stages {
        stage("Git Pull"){
            steps{
                git branch: 'dev',  
                url: 'https://github.com/gbelot2003/docker-laravel.git'
            }
        }
        stage("Copiando .env y Corriendo migraciones"){
            steps{
                script {
                    if(fileExists('./.env')){
                        echo "========Procesos activos, el archivo Existe========"
                    }else{
                        sh "cp ./.env.example ./.env"
                    }
                }
                
            }
        }
        stage("Creando Entorno Docker"){
            steps{
                sh "docker-compose build"
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


