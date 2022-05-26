test
test for fun
project 12 KG
This is fun
fall
Project engagement
project upgrade
ssffs

### Jenkinsfile for Quick Task
==================================
```
pipeline {
  agent any

  stages {
    stage("Initial cleanup") {
      steps {
        dir("${WORKSPACE}") {
          deleteDir()
        }
      }
    }   
    stage('Build') {
      steps {
        script {
          sh 'echo "Building Stage"'
        }
      }
    }

    stage('Test') {
      steps {
        script {
          sh 'echo "Testing Stage"'
        }
      }
    }
    stage('package'){
      steps {
        script {
          sh 'echo "Packaging App"'
        }
      }
    }
    stage('deploy'){
      steps{
        script{
          sh 'echo "Deploying to Dev"'
        }
      }
    }
    stage('Clean Workspace after build'){
      steps{
        cleanWs()
      }
    }
  }
}
```