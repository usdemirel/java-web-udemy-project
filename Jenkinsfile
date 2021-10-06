pipeline{
  agent any
  stages{
    stage("Build"){
      steps{
        sh 'mvn clean package'
      }
    }
    stage("Deploy"){
      steps{
        deploy adapters: [tomcat7(credentialsId: 'a1bf6135-5ca4-4a53-9276-4e98b9e46620', path: '', 
        url: 'http://ec2-3-21-122-77.us-east-2.compute.amazonaws.com:8080/')], 
        contextPath: 'javawebapplication', war: '**/java-web-udemy-project.war'
      }
    }
  }
}
