pipeline{


agent any


    tools{
        maven 'Maven3'
        jdk 'JDK21'

    }


    stages{
        stage('Checkout scm'){
            
            steps{
             git branch: 'main', url: 'https://github.com/RRitsolution/simplemavenproject.git'
        }

    }
    stage('change directory'){
        steps{
            
            sh 'cd my-app'
        }
    }

    stage('Build maven package'){
        steps{
            sh 'mvn clean package'
        }
    }
    }
    
    post {
        success {
            echo "Build successful! Artifact is in target/ folder."
        }
        failure {
            echo "Build failed."
        }
    }
}

