pipeline {
  agent any
  stages {
    stage('Source') { 
      steps {
			// Adding checkout
	        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/RICHASHRI2211/jenkins2-course-spring-boot.git']]])

      }
    }
    stage('Compile') { 
      tools {
        // Specify Tool Name from your global tool configuration
		jdk 'JDK8'
       		maven 'Maven'
      }
      steps {
			// Some Step
      }
    }
  }
}
