pipeline {
    agent any
    stages
    {
        stage ('cloning from github')
        {
            steps
            {
                git url:'https://github.com/vamsikumar1441/javawar1.git'
            }
        }
        stage ('Building the code')
        {
            steps
            {
                sh 'mvn clean install'
            }
        }
        stage ('Deploying the artifact')
        {
            steps
            {
                sh 'cp -R /root/.jenkins/workspace/Pipeline1/target/* /opt/apache-tomcat-9.0.45/webapps/'
            }
        }
    }
}
