node {
    stage('continous.download') 
    {
    git 'https://github.com/Rushav717/collabproj.git'
    }
    stage('continous.build') {
    sh 'mvn package'
    }
    stage('continous.deployment') 
    {
deploy adapters: [tomcat9(credentialsId: '49ccd05d-877b-47c3-881d-18b5f9fe1815', path: '', url: 'http://13.60.33.117:8080')], contextPath: '/devenv', war: '**/*.jar'
    }
}
