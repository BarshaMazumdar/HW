node{
   stage('SCM Checkout'){
     git 'https://github.com/BarshaMazumdar/HW.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Slack Notification'){
       slackSend baseUrl: '',
       channel: '#jenkins',
       color: 'good', 
       message: 'Welcome to Jenkins, Slack!', 
       teamDomain: 'vedantek',
       tokenCredentialId: 'slack'
   }
}
