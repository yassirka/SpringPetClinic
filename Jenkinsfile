pipeline{
agent{

label 'master'
}
tools{

maven 'M3'

}
stages{
	stage('Checkout'){
steps{

git branch: 'main', url: 'https://github.com/yassirka/SpringPetClinic.git'
}
}

	stage('Build'){
steps{

bat 'mvn.cmd compile'
}
}

stage('Test'){

steps{
bat 'mvn.cmd test'
}
}

stage('Package'){
steps{
bat 'mvn.cmd package'


}
}
stage('Deploy'){
steps{
bat 'java -jar "c:\\Users\\yakardan\\.jenkins\\workspace\\PetclinicdeclarativePipeline\\target\\spring-petclinic-2.1.0.BUILD-SNAPSHOT.jar"'
}
}
}
}
