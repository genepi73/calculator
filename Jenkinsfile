pipeline {
     agent any
     stages {
          stage("Compile") {
               steps {
                    sh "./gradlew compileJava"
               }
          }
          stage("Unit test") {
               steps {
                    sh "./gradlew test"
               }
          }
          stage("SonarQube analysis") {
     		steps {
          		sh "./gradlew sonarqube   -Dsonar.host.url=http://applb-dockerresgroup.westeurope.cloudapp.azure.com:9000   -Dsonar.login=3b262ea4d6eba43f8e8a57e9f2e8f2c65ca493e1"
    		}
	  }
     }
}
