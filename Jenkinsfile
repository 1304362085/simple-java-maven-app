pipeline {
    agent {
        docker {
            image 'maven' 
            args '-v /root/.m2:/root/.m2 -v /var/jenkins_home/settings.xml:/root/.m2/settings.xml' 
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
