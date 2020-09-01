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
      }
    }
  }
}
