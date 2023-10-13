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
      git 'clone https://github.com/wakaleo/game-of-life.git '
      echo 'scm checkout success'
      '''
    }
  }
  
  stage ('build check'){
    steps {
    sh '''
    cd/home/ec2-user/game-of-life
      mvn install
      ''' 
      echo 'build done'
    }
  }

   stage('Deploy') {
            steps {
            sh ' cp game-of-life/gameoflife-web/target/gameoflife.war  /mnt/apache-tomcat-9.0.80/webapps ' 
			
            }
        }		
}
}
    




