pipeline {
	agent any
	stages{

		stage('clone and clean repo'){
			steps {
				cleanWs()
				sh "git clone -b master https://github.com/feridromdhane/livraisonContinue1.git"
			}
		}

	stage('Build')
		{
			steps{
				script{
					sh "ansible-playbook livraisonContinue/ansible/build.yml -i livraisonContinue/ansible/inventory/host.yml"
				}
			}
		}

	}
}
