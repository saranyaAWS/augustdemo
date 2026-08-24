pipeline{
    agent any 
    stages{
        stage('git'){
        step{
           sh 'git credentialsId: 'github_creds', url: 'https://github.com/saranyaAWS/augustdemo.git'
           echo "git succeffully" 
        }
        }
        stage("version"){
        step{
           sh 'java --version'
        }
        }
        stage('build'){
        step{
            sh 'mvn clean package'
            echo "mvn initalized"
        }
        }
        stage('deploy'){
        step{
            sh 'cp target/classes App'
        }
        }
    }
}
