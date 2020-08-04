pipeline {
    agent {
        docker {
            image 'maven:3.5.2-jdk-8' 
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
