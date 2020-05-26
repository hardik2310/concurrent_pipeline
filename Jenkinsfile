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
                    agent none
                    steps {
                        echo "steps"
                        println "for run test"
                    }
                
                    post {
                        always {
                            echo "always run for windows"
                        }
                    }
                }
            }
        }
   }
}
