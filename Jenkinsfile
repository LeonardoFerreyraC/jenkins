pipeline {
    agent any
    tools { 
        maven 'MAVEN_3_6_3' 
        jdk 'JDK_1_11' 
    }
    
    stages {
        stage ('Compile Stage 2023-02') {
            steps {
                withMaven(maven : 'MAVEN_3_6_3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage 2023-02') {
            steps {
                withMaven(maven : 'MAVEN_3_6_3') {
                    sh 'mvn test'
                }
            }
        }

        stage ('package Stage 2023-2') {
            steps {
                withMaven(maven : 'MAVEN_3_6_3') {
                    sh 'mvn package'
                }
            }
        }
    }
}
