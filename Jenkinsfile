node{
  stage ('Cloning the repository'){
	git 'https://github.com/jaganreddy556/eShopOnWeb.git'
  }
  stage ('Restore Nuget') {
	bat 'c:/nuget.exe restore eShopOnWeb.sln'
  }
	stage ('Build'){
		
		bat "\"${tool 'MSBuild'}\" eShopOnWeb.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"
  }
}