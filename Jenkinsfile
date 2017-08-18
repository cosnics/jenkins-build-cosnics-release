pipeline {
    agent any 

    stages {
        stage('Zip') { 
            steps { 
                sh 'tar --exclude=\'files/configuration/configuration.xml\' --exclude=\'generatedJUnitFiles\' --exclude=\'build-reports\' --exclude=\'storage/*\' -czvf ./release.tar.gz -C /cosnics/master/current .'
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
