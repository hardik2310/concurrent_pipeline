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
                        build job: 'hardik_build_python'
                    }
                }
                stage('Test On Linux') {
                    steps {
                        echo "steps"
                        println "running in linux test" 
                        sleep(time:1,unit:"SECONDS")
                        build job: 'hardik_build_python'                       
                    }
                }
            }
        }
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
        }
    }
}
