node {
    stage('Download code from GIT Url') {
    git branch: 'release', url: 'https://github.com/clouddevopseng/new-boa.git'
     }
    stage('Convert into Artifacts using maven') {
    sh 'mvn package'
     } 
    stage('Copy or Deploy artifacts into Tomcatserver') {
    deploy adapters: [tomcat9(path: '', url: 'http://localhost:9090')], contextPath: '/dep-dev', war: '**/*.war'
     }
}
