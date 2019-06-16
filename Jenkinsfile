
node{
  stage('SCM Checkout'){
  git 'https://github.com/sunila12/my-app'
  }
  stage('Compile-Package'){
  def mvnHome = tool name: 'maven-3', type: 'maven'
  sh "${mvnHome}/bin/mvn package"
  }
  stage('Email Notification'){
    mail bcc: '', body: '''Hello, Welcome to Jenkins Notification Alert

Thanks
Sunil''', cc: '', from: '', replyTo: '', subject: 'Jenkins-job status', to: 'sunila.mahapatra@gmail.com'
  }
}

