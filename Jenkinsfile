node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		bat 'nuget restore AddToCart.sln'
		//bat "\"${tool 'MSBuild'}\" AddToCart.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"

}
