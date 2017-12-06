@Library('workshop') _
import org.skat.*


node {
    stage ('Checkout'){
        echo 'Checkout'
		
		//echo bat(returnStdout: true, script: 'env')
		echo  "${env.BUILD_NUMBER}"
		echo  "${env.BRANCH_NAME}"
		if("master".equals("${env.BRANCH_NAME}"))
			echo 'Branch master + "${env.BUILD_NUMBER}"
		else
			echo "Branch " + "${env.BRANCH_NAME} - ${env.BUILD_NUMBER}"
		
		//def zot = new org.skat.Zot()
		//zot.checkOut('jangarecife/Ateam.git')

        //git credentialsId: '258ed905-321d-4293-aac8-85858f77819d', url: 'git@github.com:jangarecife/jenkins-workshop.git'
        //checkout scm 
    }
}
