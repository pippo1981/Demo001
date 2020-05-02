peline {
   agent any
   environment {
       registry = "pippo1981/Demo001"
       GOCACHE = "/tmp"
   }
   stages {
       stage('Build') {
           steps {
               // Create our project directory.
               sh 'cd ${GOPATH}/src'
               sh 'mkdir -p ${GOPATH}/src/hello-world'
               // Copy all files in our Jenkins workspace to our project directory.               
               sh 'cp -r ${WORKSPACE}/* ${GOPATH}/src/hello-world'
               // Build the app.
               sh 'go build'              
           }    
       }
   }
}

