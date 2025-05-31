pipeline{
	agent any
	tools{
		maven 'maven'
	}
	stages{
		stage('checkout'){
		steps{
			git branch : 'master', url :'https://github.com/Manoharr108/MavenApp'
		}}
		stage('build'){
		steps{
			sh 'mvn clean package'
		}}
		stage('test'){
		steps{
		sh 'mvn test'}
		}
		stage('Run Application'){
		steps{
		sh 'java -cp target/HelloMaven-1.0-SNAPSHOT.jar com.example.App '
		}}
		
	}
}
