pipeline {
    agent any
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('git') {
              steps {
                git branch: 'main', url: 'https://github.com/Rambabu1969/new-test-jenkins.git'
            }
        }
         stage('deploy on Remote Server (http://13.233.112.233/102)') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: 'LinuxWebServer', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/var/www/html/102', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/**')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}
