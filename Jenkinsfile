pipeline {

  agent any
  
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          echo "test"
      }
    }

     stage('Deployment') {

      steps {
            bat 'mvn -U -V -e -B -DskipTests deploy -Pdev -DmuleDeploy'
      }
    }
  }
}