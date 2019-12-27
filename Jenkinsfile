pipeline {
  agent any
	statges{
    stage('Source') { 
      steps {
			// Adding checkout
	        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/RICHASHRI2211/jenkins2-course-spring-boot.git']]])

      }
    }
	  def project_path = "spring-boot-samples/spring-boot-sample-atmosphere"
	  dir(project_path){
		  
	      stage('Compile') { 
      tools {
        // Specify Tool Name from your global tool configuration
		jdk 'JDK8'
       		maven 'Maven'
      }
      steps {
		// maven build
	      powershell label: '', script: 'mvn clean package'
      }
		      
	  }

	  }    
	}
}
