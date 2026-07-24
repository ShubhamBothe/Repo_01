pipeline {
 
    agent {label "python"}
     pollSCM('H/3 * * * *')

    environment {

    APP="Inventory"

    ENV="Development"

}

    stages {
 
        stage('Welcome') {
 
            steps {

                script {

                        def app="Shopping"

                        def version="1.0"

                        echo app

                        echo ENV

                    }
 
                echo "Welcome to Jenkins Pipeline"
 
            }
 
        }
 
    }
 
}
 