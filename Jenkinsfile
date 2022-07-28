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
    }
}
