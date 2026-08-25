pipeline{
    agent any 
    stages{
        stage('git'){
        steps{
           git credentialsId: 'github_creds', url: 'https://github.com/saranyaAWS/augustdemo.git'
           echo "git succeffully" 
        }
        }
        stage("version"){
        steps{
           sh 'java --version'
        }
        }
        stage('build'){
        steps{
            sh 'mvn clean package'
            echo "mvn initalized"
        }
        }
        stage('deploy'){
        steps{
            sh 'java -cp -r target/classes App'
        }
        }
    }
}
