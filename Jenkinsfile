try{
    node {
    echo 'Build Started'
    stage('Checkout'){
         git branch: 'master', credentialsId: 'bitbucket', url: 'https://github.com/devopstrainingblr/Ant-WebProject.git'
    }
   
        stage('build'){
        bat 'ant -f build-mt.xml'
    }
     stage('Test'){
      /*  sh 'mvn test' */
         echo 'test done'
    }
    stage('Package'){
       /* sh 'mvn package' */
        echo 'Package done'
    }
    stage('Deploy-dev'){
        echo 'Deployed to dev'
    }
    stage('Deploy-stg'){
        echo 'Deployed to stg'
    }
    stage('Deploy-prod'){
        echo 'Deployed to prod'
    }
    
    
  }
}catch(error){
   echo 'Some error' 
   throw error
}
