node('JDK8') {
    stage('git-clone') {
        // build steps
        git branch: '*/sprint1_develop', credentialsId: '96b0a0e2-9ccc-4c85-a692-062abf7d44e3', url: 'https://github.com/vishnuvardhan8522/game-of-life.git'
    }
    stage('maven-package') {
        //maven package on shell
        sh 'maven package'

    }
    stage('archiving the artifacts') {
        archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false

    }
    stage('archiving the artifacts') {
    junit '**/surefire-reports/*.xml'
    }
}