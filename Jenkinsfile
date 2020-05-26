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
                    agent any
                    steps {
                        echo "steps"
                        println "running in windows test"
                        build job: 'hardik_build_python'
                    }
                }
                stage('Test On Linux') {
                    agent any
                    steps {
                        echo "steps"
                         println "running in linux test"                   
                         build job: 'hardik_build_python'                       
                    }
                }
                
            }
        }
   }
}
