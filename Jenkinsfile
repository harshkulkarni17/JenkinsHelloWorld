pipeline {
    agent any 
    stages {
        stage('Parallel Execution'){
            steps{
                parallel (
                    Build: {
                        echo "In Build Stage"
                    },
                    Test: {
                        echo "In Test Stage"
                    },
                    Deploy: {
                        echo "In Deploy stage"
                    }
                )    
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
