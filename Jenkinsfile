pipeline {
  agent any
  tools {
    maven 'M2_HOME'
  }
  stages {
    stage('build'){
      steps {
        sh 'mvn clean'
        sh 'mvn install'
        sh 'mvn package'
      }
    }
    stage('test'){
      steps {
        echo " test "
        sh 'mvn test'
        sleep 10
      }
    }
    stage('docker'){
      steps {
        echo " docker 1 2 3"
        sleep 10
      }
    }
    post {
        always {
            echo "Always display this message "
        }
        failure {
            echo "Job failed "
        }
        success {
            echo "Successful run "
        }
        unstable {
            echo "The job is unstable "
        }
    }
  }
}
