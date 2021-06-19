pipeline{
    agent{label "master"}
    tools{maven "M3"}
    stages{
        stage("XXechouTT"){
            steps{
                git branch: "main",url:"https://github.com/Mikael-Helin/SpringPetClinic.git"
            }
        }
        stage("this is da BUILD"){
            steps{
                sh "mvn compile"
            }
        }
        stage("Testen"){
            steps{
                sh "mvn test"
            }
        }
        stage("Package"){
            steps{
                sh "mvn package"
            }
        }
        stage("Deploya"){
            steps{
                sh "java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar"
            }
        }
    }
}
