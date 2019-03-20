node {

    stage('Initialize')
    {
        def dockerHome = tool 'docker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }

    stage('Build') 
    {
      sh 'uname -a'
      sh 'docker build .'
    }

    stage('Test') 
    {
      sh 'ifconfig' 
    }

    stage('Scan')
    {
      twistlockScan ca: '', cert: '', compliancePolicy: 'high', dockerAddress: 'unix:///var/run/docker.sock', gracePeriodDays: 0, ignoreImageBuildTime: false, image: 'ubuntu', key: '', logLevel: 'true', policy: 'high', requirePackageUpdate: true, timeout: 10
    }
}
