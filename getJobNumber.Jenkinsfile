node {
    stage('Run') {
        def buildName = Jenkins.instance.getItemByFullName('Jobs/Print Job Name')
        echo "Last build number: ${buildName.getLastBuild().number}"
    }
}