pipeline{
    agent any
    
    stages{
        stage('git')
        {
            steps{
                git credentialsId: '9ac6f07c-b28c-4efb-9a69-43bcba7e7142', url: 'https://github.com/bhoomikakrishnappa/mvnrepo.git'
            }
        }
        stage('validate')
        {
            steps{
                sh "mvn validate"
            }
            
         }
        stage('compile')
        {
            steps{
                sh "mvn compile"
            }
            
         }
            stage('Test')
            {
                steps{
                    sh "mvn test"
                }
            }
        stage('package')
        {
            steps{
                sh "mvn package"
            }
        }     
    }
}
