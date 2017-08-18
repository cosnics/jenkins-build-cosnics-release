pipeline {
    agent any 

    stages {
        stage('Zip') { 
            steps { 
                sh 'tar -C /cosnics/master/current --exclude=\'files/configuration/configuration.xml\' --exclude=\'generatedJUnitFiles\' --exclude=\'build-reports\' --exclude=\'storage/*\' -czvf ./release.tar.gz *'
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
