// Jenkinsfile for my-app2:
pipeline{
  agent any
  stages{
    stage('---clean---'){
      steps{
        //POM: Here we not cloned repo, Coz, automatically
        // through job during Jenkinsfile specification.
        sh 'mvn clean'
      }
    }
    stage('---test---'){
      steps{
        sh 'mvn test'
        // POM: here we not given: sh 'mvn test -f my-app2'
        // Coz, all the files are already cloned into job
        // named folder inside workspace of jenkins.
      }
    }
    stage('---package---'){
      steps{
        sh 'mvn package'
      }
    }
    stage('---deploy to tomcat---'){
      steps{
        sh 'cp -r **/*.jar /opt/tomcat/webapps/'
      }
    }
  }
}
