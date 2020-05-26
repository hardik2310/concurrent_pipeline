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
                stage('hardik build python 1') {
                    steps {
                        echo "steps" 
                        //sleep(time:50,unit:"SECONDS")
                        println "running in linux test"
                        build job: 'hardik_build_python'                       
                    }
                }
                stage('rahul job 1') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'Docker-Slave-Rahul-Test-1'
                    }
                }
                stage('rahul job 2') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'Docker-Slave-Rahul-Test-2'
                    }
                }
                stage('rahul job 3') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'Docker-Slave-Rahul-Test-3'
                    }
                }
                stage('rahul job 4') {
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'Docker-Slave-Rahul-Test-4'
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
