node{
    stage("SCM") {
        git branch: "master", url: "https://github.com/Supawich2307/docker_compose_api.git"
    }
    stage('Run'){
        step([$class: 'DockerComposeBuilder', 
        dockerComposeFile: 'docker-compose.yml', 
        option: [$class: 'StartAllServices'], 
        useCustomDockerComposeFile: true])
    }
}
