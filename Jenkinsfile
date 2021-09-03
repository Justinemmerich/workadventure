    pipeline {
        agent any
        stages {
            stage('Clean Up') { 
                steps {
                    catchError {
                        sh 'docker container stop $JOB_NAME'
                        sh 'docker container rm $JOB_NAME'
                    }
        
                }
            }

            stage('Run') { 
                steps {
                    sh 'docker-compose up -d' 
                }
            }
        }
    }
