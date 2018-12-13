pipeline {
	agent any
	stages {
	   stage ('compile stage') {
	    steps {
	      withMaven(maven: 'maven') {
		sh 'mvn clean compile'
	      }
	    }   
	   }
	
	   stage ('Testing stage') {
            steps {
              withMaven(maven: 'maven') {
                sh 'mvn test'
              }
            }
           }

	   stage ('package stage') {
            steps {
              withMaven(maven: 'maven') {
                sh 'mvn package'
              }
            }
           }

	   stage ('deployment stage') {
            steps {
              withMaven(maven: 'maven') {
                sh 'mvn deploy'
              }
            }
           }

	}
}
