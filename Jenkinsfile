pipeline {
    agent any
    tools{
        jdk "OracleJDK11"
        maven "MAVEN3"
    }
    
    environment{
        SNAP_REPO = 'vprofile-snapshot'
        NEXUSLOGIN = credentials('nexuslogin')
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'devops@123'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vprofile-maven-central'
        NEXUS_GRP_REPO = 'vprofile-maven-group'
        NEXUSIP='nexus01'
        NEXUSPORT = '8081'
        NEXUS_LOGIN='nexuslogin'
    }

    stages {
        stage("Build"){
             steps{
                sh "mvn -s settings.xml -DskipTests install"
             }
        }
    }
}