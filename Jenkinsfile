node{
   stage('SCM Checkout'){
     git 'https://github.com/hello2parikshit/myapp/blob/master/Jenkinsfile'
   }
   
    stage('Sanity check') {
      steps {
        input "Does the staging environment look ok?"
      }
    }

   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'Maven-Default', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      Thanks
      Hari''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'parixitpatel@gmail.com'
   }
  
}
