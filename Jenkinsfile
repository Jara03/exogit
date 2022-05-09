node {
    stage('Fetch repository'){
        checkout scm
    }
    stage('Build'){
        sh "mvn package -D skipTests"
    }
    stage('Tests'){
        sh "mvn test"
    }
}