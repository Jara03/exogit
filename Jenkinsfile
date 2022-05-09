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
    stage("Deploy"){
        configFileProvider([configFile(fileId:"owo", variable: 'MAVEN_SETTINGS')]) {
        // Exécuter la commande mvn avec le settings
      sh "mvn -s $MAVEN_SETTINGS -Preposilite"
    }
}