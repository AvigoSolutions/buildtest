pipeline {
    agent any
    stages {
		stage('Preparation'){
			checkout([$class: 'GitSCM', branches: [[name: '*/buildtest']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'MaheGitUsrPwd', url: 'https://github.com/AvigoSolutions/core-repo.git']]])
			checkout([$class: 'GitSCM', branches: [[name: '*/buildtest']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'MaheGitUsrPwd', url: 'https://github.com/AvigoSolutions/trial-rf.git']]])
			checkout([$class: 'GitSCM', branches: [[name: '*/buildtest']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'MaheGitUsrPwd', url: 'https://github.com/AvigoSolutions/study-sites.git']]])
			checkout([$class: 'GitSCM', branches: [[name: '*/buildtest']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'MaheGitUsrPwd', url: 'https://github.com/AvigoSolutions/frontend-host.git']]])
		}
		stage('Build') {
            steps {
				sh 'echo "Build echo";'
            }
        }
		stage('Test') {
            steps {
                sh 'echo "No Test to run!";'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Nothing to depoy!";'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}

