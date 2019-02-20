node{
   stage('SCM Checkout'){
     git 'https://github.com/manchala4444/game'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Slack Notification'){
      slackSend baseUrl: 'https://hooks.slack.com/services/',
         channel: 'jenkins', 
         color: 'good', 
         message: 'Welcome to jenkins slack', 
         teamDomain: 'jenkinshomecloud', 
         tokenCredentialId: 'slack-demo1'
   }
   
   
   }
