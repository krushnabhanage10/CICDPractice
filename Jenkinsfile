pipeline {
   agent none
   stages {
      stage('Build') {
         agent {node{label 'master'}}
        steps {
          echo 'Building...'
          sh 'hostname -i'
		  sh 'cat /etc/os-release'
		  sh 'uptime'
		  sh 'df -h'
        }
   }
   stage('Test') {
          agent {node{label 'rhel'}}
     steps {
        echo 'Testing...'
		  sh 'hostname -i'
		  sh 'cat /etc/os-release'
		  sh 'uptime'
		  sh 'df -h'
     }
   }
   stage('Deploy') {
          agent {node{label 'centos'}}      
     steps {
       echo 'Deploying...'
	      sh 'hostname -i'
	      sh 'cat /etc/os-release'
		  sh 'uptime'
		  sh 'df -h'
     }
   }
  }
}
