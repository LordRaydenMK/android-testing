#!groovy
node {
	stage 'Build'
	sh './gradlew assemble'

	stage 'Test'
	sh './gradlew test'
}
