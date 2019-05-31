# Jenkinsfile for my-app2:
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
        // Coz, We are already inside the folder my-app2
      }
    }
    stage('---package---'){
      steps{
        sh 'mvn package'
      }
    }
  }
}
