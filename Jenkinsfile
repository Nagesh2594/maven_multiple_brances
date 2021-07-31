node('master') 
{
    stage('ContinuousTesting_Master')
    {
        git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
        sh 'java -jar /root/.jenkins/workspace/ScriptedPipeline/testing.jar'
    }
    stage('COntinuousDelivery_Master')
    {
        sh 'scp /root/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war ubuntu@172.31.46.189:/var/lib/tomcat8/webapps/prodapp.war'
    }

}
