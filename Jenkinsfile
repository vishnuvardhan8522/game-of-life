node('JDK8') {
    stage('git-clone') {
        // build steps
        git branch: '*/sprint1_develop', url: 'https://github.com/vishnuvardhan8522/game-of-life.git'
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