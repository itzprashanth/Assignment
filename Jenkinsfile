node {
    stage('SCM Checkout'){
        git 'https://github.com/itzprashanth/node-todo.git'
    }
    stage('Install'){
        bat 'npm install'
    }
    stage('Test'){
        bat 'npm test'
    }
    stage('SonarQube analysis') {
        bat 'npm install sonarqube-scanner'
        bat 'sonar-scanner'
    }
    stage('Code Coverage'){
        bat 'npm install istanbul'
        bat 'npm test'
    }
}
