node('JDK8') {
    stage('SourceCode') {
        // get the code from git repo on the branch sprint1_develop
        git branch: 'sprint1_develop', url: 'https://github.com/vishnuvardhan8522/game-of-life.git'
    }

    stage('Build the code') {
        sh 'mvn package'
    }

    stage('Archiving and Test Results') {
        junit '**/surefire-reports/*.xml'
        archiveArtifacts artifacts: '**/*.war', followSymlinks: false
    }

}