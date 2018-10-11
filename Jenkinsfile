node{
  stage ('Cloning the repository'){
	git 'https://github.com/jaganreddy556/eShopOnWeb.git'
  }
stage ('Build'){
		bat 'c:\nuget.exe restore eShopOnWeb.sln'
		bat "\"${tool 'MSBuild'}\" eShopOnWeb.sln /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"

  }

}