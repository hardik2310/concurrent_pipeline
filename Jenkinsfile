pipeline {
    agent any
    environment {
        USE_JDK = 'true'
        ABC = 'environment variable ABC'
    }
    stages {
        stage('Run Tests') {
            parallel {
                stage('Test On Windows') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'Docker-Slave-Rahul-Test-1'
                    }
                }
                stage('Test On Linux') {
                    steps {
                        echo "steps" 
                        //sleep(time:50,unit:"SECONDS")
                        println "running in linux test"
                        build job: 'hardik_build_python'                       
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
