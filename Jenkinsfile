pipeline{
agent {node {lable 'build-in'  }  }      
stages{
  stage ('SCM Checkout') {
    steps {
sh 'git clone https://github.com/barchart/marketdata-api-js.git'
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
    




