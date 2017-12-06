node {
    stage ('Checkout'){
        echo 'Checkout'
        //git credentialsId: '258ed905-321d-4293-aac8-85858f77819d', url: 'git@github.com:jangarecife/jenkins-workshop.git'
        checkout scm 
    }
    stage ('Build'){
        docker.image('maven:3-jdk-8').inside('-v "$PWD":/usr/src/mymaven -w /usr/src/mymaven') {
        //docker.image('maven:3-jdk-8').inside{
            //docker run --rm -v $PWD:/usr/src/mymaven -w /usr/src/mymaven mvn clean package
            //-v $PWD:/usr/src/mymaven -w /usr/src/mymaven mvn clean package
            echo 'Start'
            def out = sh script: 'mvn clean package', returnStdout:true
            echo "$out"
            echo 'Slut'
        }
    }
    stage ('javadoc'){
        docker.image('maven:3-jdk-8').inside('-v "$PWD":/usr/src/mymaven') {
            sh 'mvn site'
        }
    }
}
