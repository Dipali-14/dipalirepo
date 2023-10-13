pipeline{
agent {
  node 
       { 
  label 'built-in'
       customWorkspace '/home/ec2-user'
       }
}
stages {
  stage ('SCM Checkout') {
    steps {
sh '''
       
      git clone https://github.com/barchart/aws-lambda-pdf-generator.git
      echo scm checkout success
      '''
    }
  }
  
  stage ('build check'){
    steps {
    sh '''
    cd /home/ec2-user/aws-lambda-pdf-generator
      mvn install
      ''' 
      echo 'build done'
    }
  }

   stage('Deploy') {
            steps {
            sh ' cp aws-lambda-pdf-generator/aws-lambda-pdf-generator-web/target/aws-lambda-pdf-generator.war  /mnt/apache-tomcat-9.0.80/webapps ' 
			
            }
        }		
}
}
    




