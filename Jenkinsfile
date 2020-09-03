ode
{
def mavenHome = tool name: "maven3.6.3"
stage('1. clone the code')
{
    git branch: 'development', credentialsId: 'gitcredentials', url: 'https://github.com/Goshenland-saas/maven-web-app.git'
}

stage('2. build package')
{
    sh "${mavenHome}/bin/mvn clean package"
}
stage('3. CodeQualityReport')
{
    //sh "${mavenHome}/bin/mvn sonar:sonar"
}
stage('4. UploadBuildArtifacts')
{
    sh "${mavenHome}/bin/mvn clean deploy"
}

}
