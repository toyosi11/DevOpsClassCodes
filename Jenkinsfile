pipeline{ 
 
 tools{ 
 jdk 'myjava' 
 maven 'mymaven' 
 } 
 
 agent any 
 
 stages{ 
 stage('Clone Repo') 
 { 
 steps{ 
 git 'https://github.com/toyosi11/DevOpsClassCodes.git' 
 } 
 } 
 
 stage('Compile the code') 
 { 
 steps{ 
 
 sh 'mvn compile' 
 } 
 } 
 
 stage('Code Analysis') 
 { 
 steps{ 
 sh 'mvn pmd:pmd' 
 } 
 } 
 
 stage('Build the artifact') 
 { 
 steps{ 
 sh 'mvn package' 
 } 
 } 
 } 
}
