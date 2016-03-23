node {
	stage 'Checkout'
	git branch: 'final', url: 'https://github.com/LordRaydenMK/android-testing/'

	stage 'Build'
	sh './gradlew assemble'

	stage 'Test'
	sh './gradlew test'
}
