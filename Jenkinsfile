pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs	'nodejs' 
    } 

    stages{
        stage('Build'){
            steps{
                echo 'This is the Build job'
                sh 'npm install'
            }
        }
        stage('Test'){
            steps{
                echo 'This is the Test job'
                sh 'npm test'
            }
        }
        stage('Package'){
            steps{
                echo 'This is the Package job'
                sh 'npm run package'

            }
        }
    }
    
    post{
        always{
            echo 'This pipeline has completed...'
        }
        
    }
    
}
