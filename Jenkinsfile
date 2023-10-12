pipeline{
agent any
stages{
  stage ('SCM Checkout') {
    steps {

      echo 'scm checkout success'
    }
  }
  
  stage ('build check'){
    steps {
    sh 'mvn install'
   
      echo 'build done'
    }
  }

  stage (test){
    steps {
       sh 'mvn -version'
      
    }
  }
}
}
    




