pipeline{
   agent any
   
   tools{
   maven 'Maven'
   }
   
   stages{
   stage('Checkout'){
   steps{
   git branch:'main',url:"https://github.com/amruthar77/MavenSimpleLast.git"
   }
   }
   
   stage('Build'){
   steps{
   sh 'mvn clean package'
   }
   
   }
   
   stage('Test'){
   steps{
   sh 'mvn test'
   }
   }
   
   stage('Run Application')
   {
   steps{
   sh 'java -jar target/MavenSimpleLast-1.0-SNAPSHOT.jar '
   }
   }
   }
   
   post{
   success{
   echo "success"
   }
   failure{
   echo "failure"
   }
   }
   }
