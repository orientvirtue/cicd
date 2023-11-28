pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: 'web', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/var/www/html', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/*.php')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
        stage('Log') {
            steps {
                echo 'log'
            }
        }
    }
}
