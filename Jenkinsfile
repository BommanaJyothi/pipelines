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
        echo 'executing the java file...'
        java HelloWorld
      }
    }
  stage('install'){
      steps{
        echo 'install stage....'
      }
    }
  }
}
