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
        sh '/opt/apache-maven-3.5.0/bin/mvn clean compile package'
      }
    }
  }
}