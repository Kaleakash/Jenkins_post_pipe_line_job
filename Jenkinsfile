pipeline {
    agent any
    stages {
        stage("version of software"){
            steps{
                sh "java --version"
                //bat "java --version"
            }
        }
        stage("compile java program"){
            steps{
                sh "javac Demo.java"
                //bat "javac Demo.java"
            }
        }
        stage("run the java program"){
            steps{
                sh "java Demo"
                //bat "java Demo"
            }
        }
        //  stage('Test') {
        //         steps {
        //            sh 'echo "Fail!"; exit 1'
        //         }
        //      }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'Example : if the Pipeline was previously failing but is now successful'
        }
    }
}
