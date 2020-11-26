pipeline {
    agent { label 'HRMS&&QA' }
    triggers { cron('30 * * * 1-5') }
    stages {
        stage('git'){
            steps {
                git branch: 'declarativepipeline', url: 'https://github.com/aavulasrivani/game-of-life.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}