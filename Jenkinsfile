//declarative pipeline
pipeline{
    agent {label 'master'}
    stages {
        stage('clone and compile'){
            steps {
                 git branch: 'declarative'
                 url: git 'https://github.com/practisevenkat/game-of-life.git'
                 sh 'mvn compile'
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