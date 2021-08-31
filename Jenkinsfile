pipeline {
  agent any
  tools {
    {
      nodejs "nodejs"
    }
  }

  stages {
    stage("Installation") {
      steps {
        sh 'npm install'
        echo "installing npm"
      }

      stage('Testing') {
        steps {
          sh 'npm run test -- --watchAll=false'
          echo "Testing npm"
        }
      }

      stage('Building') {
        steps {
          sh 'npm run build'
          echo "building npm "
        }
      }
    }
  }

}
