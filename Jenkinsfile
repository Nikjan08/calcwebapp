node{
	    stage('Git-Checkout'){
	        git 'https://github.com/Nikjan08/calcwebapp.git'
	    }
	    stage('Build'){
	        def mvnHome = tool name: 'MAVEN_HOME', type: 'maven'
	        bat "${mvnHome}/bin/mvn package"
	    }
	    stage('Deployment'){ 
	        bat 'copy "target\calcwebapp.war" "%CATALINA_HOME%\webapps"'
	    }
	    stage('Email-Notification'){
	      mail bcc:'', body:'''Hi Welcome to Jenkins alerts
	      Thanks
	      R.Janani''', cc:'', from:'', replyTo:'', subject:'PipeLine Job', to:'sonu.janani@gmail.com'
	    }
	    
	}

