pipeline {
  agent any
  stages {
    stage('Get Code') {
      steps {
        echo 'This is Checkout Step1'
        echo 'This is Checkout Step2'
      }
    }
    stage('Test') {
      steps {
        pwd()
      }
    }
    stage('Stage3') {
      steps {
        input 'Please approve to proceed'
      }
    }
    stage('Stage4') {
      steps {
        recordIssues(aggregatingResults: true)
      }
    }
    stage('Stage5') {
      steps {
        fileExists 'welcome.txt'
      }
    }
  }
}