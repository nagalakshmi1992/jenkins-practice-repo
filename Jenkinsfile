//CODE_CHANGES = getGitChanges()
pipeline {
  agent any
  stages {
    stage("build") {
      when {
        expression {
          BRANCH_NAME == 'dev' 
        }
        
      }
      steps {
        echo "welcome to build stage from dev branch"
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
