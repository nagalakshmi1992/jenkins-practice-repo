CODE_CHANGES = getGitChanges()
pipeline {
  agent any
  stages {
    stage("build") {
      when {
        expression {
          BRANCH_NAME == 'dev' && CODE_CHANGES == 'true'
        }
        
      }
      steps {
        echo "welcome to build stage"
      }
      
    }
    stage("test") {
      steps {
        echo "welcome to test stage"
      }
      
    }
  }
  post {
    always {
      echo "this will always executes"
    }
  
  }
  
}
