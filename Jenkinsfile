pipeline {
   agent { label 'jenkins-agent' }
   tools {
        jdk 'java17'
        maven 'Maven3'
    }
    satges{
      stage("Cleanup Workspace"){
              steps {
              cleanWs()
                }
}

  stage("Checkout from SCM"){
     step {
              git branch: 'main', crendentialsId: 'github', url: 'https://github.com/avinashgaikwad9441/Project1.git'
          }
}
   stage("Build Application"){
            steps {
                sh "mvn clean package"
            }

       }

       stage("Test Application"){
           steps {
                 sh "mvn test"
           }
       }
  )
)
