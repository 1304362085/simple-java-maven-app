pipeline {
    agent {
        docker {
            image 'maven' 
            args '-v c:\users\huituo\.m2:/root/.m2' 
        }
    }
    node {
    sh "java -version"
    sh "which java"
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests -s /var/jenkins_home/settings.xml clean package' 
            }
        }
    }
}
