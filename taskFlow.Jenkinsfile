pipeline {
    agent any
    stages{
        stage('Run Job') {
            steps {
                retry(3) {
                    build "Jobs/Print Job Name"
                }
            }
        }
        stage('Print job number'){
            steps {
                script{
                    def BUILD = build 'Jobs/Get last successfull build of Print Job Name'
                    echo "${BUILD.rawBuild.log}"
                }
            }
        }
    }
}