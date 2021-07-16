node{
    stage("SCM") {
        git branch: "master", url: "https://github.com/kartheekgottipati/Docker-compose-flask-redis-deploy.git"
    }
    stage('Run'){
        step([$class: 'DockerComposeBuilder', 
        dockerComposeFile: 'docker-compose.yml', 
        option: [$class: 'StartAllServices'], 
        useCustomDockerComposeFile: true])
    }
}
