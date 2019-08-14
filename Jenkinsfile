// Powered by Infostretch 

timestamps {

node () {

	stage ('Chinmay_Cart - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/tavisca-cpadole/AddToCart.git']]]) 
	}
	stage ('Chinmay_Cart - Build') {
 			// Shell build step
sh """ 
dotnet restore AddToCart.sln 
 """		// Shell build step
sh """ 
dotnet build AddToCart.sln -p:Configuration=release -v:q 
 """		// Shell build step
sh """ 
dotnet test CartTests/CartTests.csproj 
 """ 
	}
}
}
