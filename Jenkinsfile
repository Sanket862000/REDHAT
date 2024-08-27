pipeline {
    agent any
    triggers {
  pollSCM '* * * * *'
}
    stages {
        stage ('chekout') {
            steps {
              git 'https://github.com/Sanket862000/REDHAT.git'   
            }
        }
        stage ('build') {
            steps {
                  sh 'mvn install'

            }
        }
        stage ('Deployment') {
            steps {
         sh 'cp target/REDHAT.war /home/sanket/Documents/Devops/apache-tomcat-9.0.93/webapps'
                
            }
        }
    }
}
