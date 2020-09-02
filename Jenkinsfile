pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       NodeJS 'NodeJS 4.8.6' 
    }
    

    stages{
        stage('one'){
            steps{
                echo 'this is the build job'
                sh 'npm install'
            }
        }
        stage('two'){
            steps{
                echo 'this is the test job'
                sh 'npm install'
		sh 'npm test'
            }
        }
        stage('three'){
            steps{
                echo 'this is the packaging job'
                sh 'npm install'
		sh 'npm run package'
		archiveArtifacts '**/target/*.jar'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}

