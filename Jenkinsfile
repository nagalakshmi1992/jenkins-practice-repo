pipeline {
  agent any
  /*
  tools {
    echo "list the tools used in this pipeline"
  }
  environment {
    NEW_VERSION = '1.2'
    SERVER_CREDENTIALS = credentials('server-credentials')
   }
   */
  parameters {
    choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
    booleanParam(name: 'executeTests', defaultvalue: true, description: '')
  }  
  stages {
    stage("build") {
      steps {
        echo "welcome to build stage"
        echo " version is ${NEW_VERSION}"
        
      }
      
    }
    stage("test") {
      when {
        expression {
          params.executeTests
        }
      }
      steps {
        echo "welcome to test stage"
      }
      
    }
    stage("deploy") {
      
      steps {
        echo "welcome to deploy stage"
        echo "deploying version ${params.VERSION}"
        
      }
      
    }
  }
  
}
