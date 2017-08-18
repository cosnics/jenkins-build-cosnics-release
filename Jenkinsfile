pipeline {
    agent any 

    stages {
        stage('Zip') { 
            steps { 
                sh 'tar --exclude=\'files/configuration/configuration.xml\' --exclude=\'cache/*\' --exclude=\'generatedJUnitFiles\' --exclude=\'build-reports\' --exclude=\'storage/*\' -czvhf ./release.tar.gz -C /cosnics/master/current .'
            }
        }
        stage('Artifact'){
            steps {
                archiveArtifacts 'release.tar.gz'
            }
        }
        stage('Github (ToDo)') {
            steps {
                echo 'TODO'
            }
        }
    }
}
