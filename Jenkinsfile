pipeline{
  agent any
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
        javac HelloWorld.java
        echo 'compilation done'
        echo 'executing the java file...'
        java HelloWorld
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
