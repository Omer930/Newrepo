  pipeline{
    agent any
    tools{
       maven 'MAVEN'
    }
    
    
    stages{
        stage('Checkout'){
            
            steps{
                
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Omer930/maven-jenkins.git']]])
        }
        stage('Build'){
            
            steps{
                
                sh 'mvn -Dmaven.test.failure.ignore=true clean package'
            }
        }
        
        
      }
    
    ]
