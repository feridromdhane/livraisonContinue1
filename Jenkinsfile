pipeline {
	agent any
	stages{

		stage('clone and clean repo'){
			steps {
				cleanWs()
				sh "git clone -b master https://github.com/feridromdhane/livraisonContinue1.git"
			}
		}

		stage('docker')
		{
		  steps{
		    script{
		      sh "ansible-playbook livraisonContinue/ansible/docker.yml -i livraisonContinue/ansible/inventory/host.yml"
		    }
		  }
		}

	}
}
