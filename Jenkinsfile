pipeline {
  agent any
  environment {
    NEW_VERSION = '1.2'
   }
  stages {
    stage("build") {
      steps {
        echo "welcome to build stage"
        echo " version is ${NEW_VERSION}"
      }
      
    }
    stage("test") {
      steps {
        echo "welcome to test stage"
      }
      
    }
  }
  
}
