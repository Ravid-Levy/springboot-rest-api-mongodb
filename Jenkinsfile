node {
    def image 
    stages {
        stage('Check Git')
        {
            steps
            {
                checkout scm
            }
        }

        stage('Build Image')
        {
            steps
            {
                image = docker.build("my-image:${env.BUILD_ID}")
                

            }
        }

      stage('Test image')
      {
        /* Ideally, we would run a test framework against our image.
         * For this example, we're using a Volkswagen-type approach ;-) */

        image.inside
        {
            sh 'maven test'
        }
    }
           
}
