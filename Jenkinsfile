//declarative pipeline
pipeline{
    agent {label 'master'}
    stages {
        stage('Source'){
            steps {
                git 'https://github.com/practisevenkat/game-of-life.git'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
    }
}

// scripted pl
// node {
//     stage('scm'){
//         git 'https://github.com/practisevenkat/game-of-life.git'
//     }
//     stage('build'){
//     sh 'mvn package'
//     }
// }