#!/usr/bin/env groovy
pipeline {
node {
	stage 'Checkout'
		checkout scm

	stage 'Build'
		echo 'nuget restore SolutionName.sln'
		echo "\"${tool 'MSBuild'}\" SolutionName.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /p:ProductVersion=1.0.0.${env.BUILD_NUMBER}"

	stage 'Archive'
		echo 'ProjectName/bin/Release/**'

}
}
