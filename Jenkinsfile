node {
    def server
    def rtDocker
    def buildInfo

    stage ('Artifactory configuration') {
        // Obtain an Artifactory server instance, defined in Jenkins --> Manage Jenkins --> Configure System:
	//SERVER_ID=artifactory
        server = Artifactory.server artifactory
        // Host:
        // On OSX: "tcp://127.0.0.1:1234"
        // On Linux can be omitted or null
	//HOST_NAME=http://43.204.10.182:8082
        rtDocker = Artifactory.docker server: server, host: "http://localhost:8082"
        buildInfo = Artifactory.newBuildInfo()
    }
/*
    stage ('Pull an image from Artifactory') {
       rtDocker.pull ARTIFACTORY_DOCKER_REGISTRY + '/hello-world:latest', 'docker-remote', buildInfo
    }

    stage ('Publish build info') {
        server.publishBuildInfo buildInfo
    } */
}
