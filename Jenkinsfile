pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "Build Stage" 
            }
        }
        stage('Test') { 
            steps {
                echo "Test Stage" 
            }
        }
        stage('Deploy') { 
            steps {
                echo "Deploy Stage" 
            }
        }
        stage('User Input'){
            steps{
                input ("Do you want to run process further?")
                echo "Last Stage - User Input Done"
            }
        }
        stage ('Email'){
            steps{
                mail body:"${env.JOB_NAME} - Build#${env.BUILD_NUMBER} - ${currentBuild.currentResult}\n\nCheck console output at ${env.BUILD_URL} to view the results", subject:"${env.JOB_NAME} - Build#${env.BUILD_NUMBER} - ${currentBuild.currentResult}!!", to:'hpkulkarni1705@gmail.com'
            }
        }
    }
}
