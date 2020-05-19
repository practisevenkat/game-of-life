//declarative pipeline
pipeline{
    agent {label 'master'}
    triggers { pollSCM upstream(upstreamProjects: 'gol-1', threshold: hudson.model.Result.SUCCESS) }
    stages {
        stage('clone'){
            steps {
                 git url: 'https://github.com/practisevenkat/game-of-life.git', branch: 'declarative'
            }
        }
        stage('compile')
        {
            steps{
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