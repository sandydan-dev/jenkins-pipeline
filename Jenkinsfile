pipeline {
  agent any
 
  environment {
     PATH="/opt/maven/bin:$PATH
  }

  stages {
    // git start
    stage("git clone"){
      steps {
        echo "----- git clone start -----"
        git url: "https://github.com/sandydan-dev/jenkins-pipeline.git", branch : "main"
        echo "----- git clone end -----"
      } 
    }  
    // git end

    // build start
    stage("build"){
      steps {
        echo "----- build start -----"
        sh "mvn clean package"
        echo "----- build end -----"
      }
    }
   
 
  }
   post {
        always {
            echo "pipeline script completed"
        }
    }

}
