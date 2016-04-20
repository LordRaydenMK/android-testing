#!groovy
node {
	stage 'Checkout'
	git branch: 'master', url: 'https://github.com/LordRaydenMK/android-testing/'

	stage 'Build'
	sh './gradlew clean assemble'

	stage 'Android Lint'
	sh './gradlew lint'

	stage 'Test'
	sh './gradlew test'

	stage 'JUnit tests'
	step([$class: 'JUnitResultArchiver', testResults: 'app/build/test-results/*/TEST-*.xml'])
}
