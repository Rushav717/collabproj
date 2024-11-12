node {
    stage('cont.download')
{
    git 'https://github.com/Rushav717/collabproj.git'
}
    stage('cont.build') 
{
    sh 'mvn package'
}
    stage('cont.deployment') 
{
     deploy adapters: [tomcat9(credentialsId: 'da3f899b-3a16-49cf-bd51-b16b79bd8a4f', path: '', url: 'http://16.170.205.152:8080/')], contextPath: '/dev', war: '**/*.war'
}
     }
