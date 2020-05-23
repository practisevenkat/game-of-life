node {
    stage('scm'){
        git 'https://github.com/practisevenkat/game-of-life.git'
    }
    stage('build'){
    sh 'mvn package'
    }
    stage('sonar'){
        withSonarQubeEnv('SONAR') { 
      sh 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar'
        }
        }
}
