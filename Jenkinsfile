node {

stage('Clone Repository')
{
checkout scm
}


stage('Show me the files')
{
sh "ls -l"
}


stage('Build Docker Image and push image to DockerHub')

{
sh "docker build -t valexercise:version1"
sh "docker run -d -p 8080:80/tcp valexercise:version1"
sh "docker login -u 'vkageha' -p 'Vale1991'"
sh "docker tag valexercise:version1 vkageha/valexercise:version1"
sh "docker push vkageha/valexercise:version1"
}


stage('Apply changes to the environment')
{
sh "ls -l"
}




}



