node('master') 
{
    stage('ContinuousDownload_Master') 
    {
        git 'https://github.com/intelliqittrainings/maven.git'
    }
    stage('ContinuousBuild_Master')
    {
        sh 'mvn package'
    }
    stage('ContinuosDeployment_Master')
    {
        sh 'scp /root/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.42.41:/var/lib/tomcat8/webapps/testapp.war'
    }
}
