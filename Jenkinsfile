node{
    stage("SCM") {
        git branch: "master", url: "https://github.com/Supawich2307/docker_compose_api.git"
    }
    stage('Run'){
        sh "./deploy.sh"
    }
}
