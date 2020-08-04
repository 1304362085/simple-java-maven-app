pipeline {
    agent {
        docker {
            image 'maven:3.5.2-jdk-8' 
            args '-v //c/Users/huituo/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            agent{
               // def mvnHome = tool 'M3.2.3'
                // 这里就是引入我们在全局配置中配置的jdk；写法：tool 名称
                def jdk88 = tool 'jjdk'
                // 再把变量加入到环境变量中
                env.PATH = "${jdk88}/bin:${mvnHome}/bin:${env.PATH}"
                sh "mvn -B verify"
                sh "echo '$PATH'"
                sh "which java"
                //sh "echo ${JOB_NAME}"
                //sh "echo ${env.JOB_NAME}"
            }
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
