pipeline {
    agent any
    environment {
        USE_JDK = 'true'
        ABC = 'environment variable ABC'
    }
    stages {
        stage('Run Tests') {
           
            parallel {
                stage('hardik build python 1') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'hardik_build_python'
                    }
                }
                stage('hardik build python 2') {
                    steps {
                        echo "steps" 
                        //sleep(time:50,unit:"SECONDS")
                        println "running in linux test"
                        build job: 'hardik_build_python'                       
                    }
                }
                stage('docker job 1') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'hardik-docker-1'
                    }
                }
                stage('docker job 2') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'hardik-docker-2'
                    }
                }
                stage('docker job 3') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'hardik-docker-3'
                    }
                }
                stage('docker job 4') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'hardik-docker-4'
                    }
                }
            }
        }
       /* 
        stage('con-current1') {
            steps {
                echo 'Building con-current 1..'
                build job: 'hardik_build_python'     
            }
        }
        stage('con-current2') {
            steps {
                echo 'Building con-current 2..'
                build job: 'hardik_build_python'     
            }
        }*/
    }
}
