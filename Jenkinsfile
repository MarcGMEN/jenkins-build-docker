
node {

  
   def IMAGE="srv-web-marc"
	
    stage('Clone') {
          checkout scm
    }

    stage('Build') {
          docker.build("$IMAGE",  '.')
    }

    stage('Run image') {
        docker.image('srv-web-marc').withRun('--name srv_web-marc' ) { c ->

        sh 'docker ps | grep srv_web-ano'
	}

    }
}
