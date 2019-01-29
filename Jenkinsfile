node{
	    stage('Git-Checkout'){
	        git 'https://github.com/Nikjan08/calcwebapp.git'
	    }
	    stage('Compile-Test'){
	        def mvnHome = tool name: 'MAVEN', type: 'maven'
	        bat "${mvnHome}/bin/mvn package"
	    }
	    stage('Deployment'){ 
	        bat 'copy target/*.war tomcat9/webapps'
	    }
	    stage('Email-Notification'){
	      mail bcc:'', body:'''Hi Welcome to Jenkins alerts
	      Thanks
	      R.Janani''', cc:'', from:'', replyTo:'', subject:'PipeLine Job', to:'sonu.janani@gmail.com'
	    }
	    
	}

