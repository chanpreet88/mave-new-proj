


 
stage('prep') {

checkout scm 

}

stage('compile') { 
 
def myTestContainer = docker.image('maven:3.2-jdk-7')

myTestContainer.pull()
 

myTestContainer.inside("-w /usr/src/mymaven" ) {

sh 'mvn compile'

}
}

stage('package') { 

myTestContainer.inside("-w /usr/src/mymaven" ) {

sh 'mvn package'

}
}




