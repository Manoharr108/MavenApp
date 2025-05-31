pipeline{
	agent any
	tools{
		maven 'maven'
	}
	stages{
		stage('checkout'){
			git branch : 'master', url :'https://github.com/Manoharr108/MavenApp'
		}
		stage('build'){
			sh 'mvn clean package'
		}
		stage('test'){
		sh 'mvn test'
		}
		stage('Run Application'){
		sh 'java -cp target/HelloMaven-1.0-SNAPSHOT.jar com.example.App '
		}
		
	}
}
