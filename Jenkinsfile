pipeline {
  agent any
  stages {
    stage('SCM Download') {
      steps {
        git(url: 'https://github.com/indexit-devops/mavenrepo', branch: 'master', poll: true)
      }
    }
    stage('BUILD') {
      steps {
        sh 'mvn clean compile package'
      }
    }
  }
}