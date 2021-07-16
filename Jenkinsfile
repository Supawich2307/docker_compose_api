node{
    stage("SCM") {
        git branch: "main", url: "https://github.com/Supawich2307/rest_api_test.git"
    }
    stage('Initialize'){
        def dockerHome = tool 'myDocker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
   //  stage("Kill Docker Container & Older image") {
   //    sh "docker kill test_rest"
   //    sh "docker rmi -f supakew/test_api:"
   //  }
    stage("Build") {
      sh "docker build -t supakew/test_api:${env.BUILD_NUMBER} ."
    }
    stage("Run") {
        sh "docker run -d -p 5200:5200 --name test_rest supakew/test_api:${env.BUILD_NUMBER}"
    }
}