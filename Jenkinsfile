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
    booleanParam(name: 'executeTests', defaultValue: true, description: '')
  }  
  stages {
    stage("init") {
      steps {
        script {
        gv = load "script.groovy"
        }
               
      }
      
    }
    stage("build") {
      steps {
        //echo "welcome to build stage"
        //echo " version is ${NEW_VERSION}"
        gv.buildApp()
        
      }
      
    }
    stage("test") {
      when {
        expression {
          params.executeTests
        }
      }
      steps {
        gv.testApp()
      }
      
    }
    stage("deploy") {
      
      steps {
        //echo "welcome to deploy stage"
        echo "deploying version ${params.VERSION}"
        gv.deployApp()
        
      }
      
    }
  }
  
}
