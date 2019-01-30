node{
	    stage('Git-Checkout'){
	        git 'https://github.com/Nikjan08/calcwebapp.git'
	    }
	    stage('Build'){
	        def mvnHome = tool name: 'MAVEN', type: 'maven'
	        sh "${mvnHome}/bin/mvn package"
	    }
	    stage('Deployment'){ 
	        sh 'cp target/*.war /opt/tomcat9/webapps'
	    }
	    stage('Email-Notification'){
	      mail bcc:'', body:'''Hi Welcome to Jenkins alerts
	      Thanks
	      R.Janani''', cc:'', from:'', replyTo:'', subject:'PipeLine Job', to:'sonu.janani@gmail.com'
	    }
	    
	}

