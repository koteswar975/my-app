node('test1_maven'){
   
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
      // Get maven home path
      sh "mvn clean package"
   }
   stage('Email Notification'){
   emailext body: '$build', subject: 'Test build', to: 'koteswarreddy40@gmail.com'
   }
}
