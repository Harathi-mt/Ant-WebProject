try{
    node {
    echo 'Build Started'
    stage('Checkout'){
         git branch: 'master', credentialsId: 'bitbucket', url: 'https://github.com/devopstrainingblr/Ant-WebProject.git'
    }
    stage('Build'){
    /* bat "ant -f build-mt.xml" */ /*For windows machines*/
    bat "ant -f build-mt.xml" 
 }
  }
}catch(error){
   echo 'Some error accured' 
   throw error
}
