def VERSION = "1.0.0"
pipeline {
    agent any
  tools {
    maven 'maven3'
	}
	stages{
	    stage('Build') {
		  steps{
		      sh 'mvn clean package'
			  script {
                    VERSION = readMavenPom().getVersion()
                }
                echo("Build version: ${VERSION}") 
      }
      }
	  }
	  }
	    
