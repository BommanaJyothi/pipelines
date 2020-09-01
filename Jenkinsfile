pipeline{
  agent any
  tools {
        // Install the java version configured as "localSDK" and add it to the path.
        jdk "localSDK"
    }
  stages {
    stage('build'){
      steps{
        echo 'build stage....'
        echo 'hello world.'
      }
    }
  stage('compile'){
      steps{
        echo 'compile stage....'
         bat "javac HelloWorld.java"
        echo 'compilation done'
        echo 'executing the java file...'
        bat "java HelloWorld"
        echo 'executing the file...'
      }
    }
  stage('install'){
      steps{
        echo 'install stage....'
        sh "java HelloWorld"
      }
    }
  }
    
   post {
    failure {
        mail to: 'bommanajyothi999@gmail.com',
             subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
             body: "Hello Developer, \n Something is wrong with ${env.BUILD_URL}"
      }
     success {
        mail to:'bommanajyothi999@gmail.com',
       subject: "Success Pipeline: ${currentBuild.fullDisplayName}",
       body: "Hello Developer,\n The pipeline is success. The pipeline URL is ${env.BUILD_URL}"
     }
      always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
    }
}
