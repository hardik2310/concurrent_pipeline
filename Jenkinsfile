pipeline {
    agent any
    environment {
        USE_JDK = 'true'
        ABC = 'environment variable ABC'
    }
    stages {
        stage('Run Tests') {
            parallel (
                // job 1, 2 and 3 will be scheduled in parallel.
                { build("hardik_build_python") },
                { build("hardik_build_python") },
                { build("hardik_build_python") }
            )
            /*
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
                        //sleep(time:50,unit:"SECONDS")
                        println "running in linux test"
                        build job: 'hardik_build_python'                       
                    }
                }
            }*/
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
