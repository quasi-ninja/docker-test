node {

    stage('Initialize')
    {
        def dockerHome = tool 'docker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }

      stage('Build') 
           {
            sh 'uname -a'
          }

        stage('Test') 
        {
            sh 'ifconfig' 
        }
}
