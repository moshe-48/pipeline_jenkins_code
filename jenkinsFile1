node {
stage('check out code') {
checkout([$class: 'GitSCM', branches: [[name: 'master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/moshe-48/jenkins-course.git']]])
}
stage('build something'){
}
stage('test something'){
}
stage('deploy'){
    parallel deploy_to_DEV: {
        try{
            sh 'echo "deploy to dev"'
        }
        finally{
            sh 'echo "finished this stage"'
        }
        
    },
    deploy_to_QA: {
        try{
            sh 'echo "deploy to qa"'
        }
        finally{
            sh 'echo "finished this stage"'
        }
        
    }
}
stage('package')
    chuckNorris()
}
