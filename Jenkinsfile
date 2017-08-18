pipeline {
    agent any 

    stages {
        stage('Zip') { 
            steps { 
                sh 'tar --exclude=\'/cosnics/master/current/files/configuration/configuration.xml\' --exclude=\'/cosnics/master/current/storage/*\' -czvf ./release.tar.gz /cosnics/master/current/*'
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
