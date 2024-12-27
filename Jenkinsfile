pipeline {
	
    agent any
	
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        SNAP_REPO = 'vrofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = '6451lake'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.21.98'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vrpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }

}