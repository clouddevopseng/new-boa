node {
    stage('Download code from GIT Url') {
    git branch: 'prod', url: 'https://github.com/clouddevopseng/new-boa.git'
     }
    stage('Convert into Artifacts using maven') {
    sh 'mvn package'
     } 
    stage('Copy or Deploy artifacts into Tomcatserver') {
    deploy adapters: [tomcat9(path: '', url: 'http://172.17.0.10:9090')], contextPath: '/dep-prod', war: '**/*.war'
     }
}
