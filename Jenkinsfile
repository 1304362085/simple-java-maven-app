pipeline {
    agent {
        docker {
            image 'maven' 
            args '-v /root/.m2:/root/.m2 -v /var/jenkins_home/settings.xml:/var/jenkins_home/settings.xml' 
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
