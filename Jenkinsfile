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
       
      git clone https://github.com/DependencyTrack/public-api-java.git
      echo scm checkout success
      '''
    }
  }
  
  stage ('build check'){
    steps {
    sh '''
    cd /home/ec2-user/public-api-java
      mvn install
      ''' 
      echo 'build done'
    }
  }

   stage('Deploy') {
            steps {
            sh ' cp public-api-java/public-api-java-web/target/public-api-java.war  /mnt/apache-tomcat-9.0.80/webapps ' 
			
            }
        }		
}
}
    




