node {    

    environment {
        dockerImage = ''
        //import 
        registry = 'jpk912/appointment2'
        //import docker hub credentials
        //REGISTRY_CREDENTIAL = credentials('DOCKER_ID')
    }
      //def app     
      stage('Clone repository') {               
            
            checkout scm
      }     
      stage('Build image') {    

            sh ''' #!/bin/bash
                echo "Building apache...."
            '''
            website = docker.build("jpk912/appointment2-jenkins-apache", "-f nginx/Dockerfile .")

            // sh ''' #!/bin/bash
            //     echo "Building sql...."
            // '''
            //sqldb = docker.build("jpk912/appointment2-jenkins-sqldb", "-f sql/Dockerfile .")

       }     
      stage('Test image') {           
            sh '''
                echo "Tests would go here...."
            '''  
        }     
       stage('Push image') {
           //login and push to registry. DOCKER_ID is the jenkins credentials created. No need to import into jenkinsfiles
            // docker.withRegistry('https://registry.hub.docker.com', 'DOCKER_ID') {            
            //     website.push("${env.BUILD_NUMBER}")            
            //     sqldb.push("${env.BUILD_NUMBER}")            
            //     //website.push("latest")        
            // }    
        }
}