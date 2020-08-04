pipeline {
    agent {
        node{
            sh 'which java'
        }
        docker {
            image 'maven' 
            args '-v //c/Users/huituo/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
