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
       emailext body: '''Hello Developers,
               Please find the below  pipeline URL is ${env.BUILD_URL}''', subject: '${currentBuild.fullDisplayName}', to: 'bommanamohan8106@gmail.com'
      }
     success {
        emailext body: '''Hello Developers,
               Please find the below  pipeline URL is ${env.BUILD_URL}''', subject: '${currentBuild.fullDisplayName}', to: 'bommanamohan8106@gmail.com'
     }
      always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
    }
}
