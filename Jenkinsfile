pipeline {
    agent {
        docker {
            image 'maven' 
            args '-v //c/Users/huituo/.m2:/root/.m2' 
            sh 'which java'
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
