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

        // stage('Test Image')
        // {
        //     image.inside()
        //     {
        //     sh 'echo hello'
        //     }

        // }



}
