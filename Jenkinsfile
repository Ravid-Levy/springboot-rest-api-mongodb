node {
    def image 
        stage('Check Git')
        {
            checkout scm

        }

        stage('Build Image')
        {

                image = docker.build("my-image:${env.BUILD_ID}")
        }

      stage('Test image')
      {
        image.inside
        {
            sh 'maven test'
        }
    }
        


}
