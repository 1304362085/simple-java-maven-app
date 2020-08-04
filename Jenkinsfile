pipeline {
    agent {
        docker {
            image 'maven' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests -s /var/jenkins_home/settings.xml clean package' 
            }
        }
    }
}
