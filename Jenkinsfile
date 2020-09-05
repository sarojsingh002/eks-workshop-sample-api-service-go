pipeline {
    agent any
    stages{
        stage ('Docker build'){
            steps{
                script{
                  
                        docker.build('sksrepos')
                    
                   
                }
            }
        }
        stage ('Docker push'){
            steps{
                script{
                  
                        docker.withRegistry('https://498431404772.dkr.ecr.us-west-2.amazonaws.com', 'aws-ecr1') 
                        {
                            docker.image('sksrepos').push('latest')
                        }
                    
                  
                }
            }
        }

    }
}
