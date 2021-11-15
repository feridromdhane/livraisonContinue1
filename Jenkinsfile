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
					sh "ansible-playbook livraisonContinue1/Ansible/build.yml -i livraisonContinue1/Ansible/inventory/host.yml"
				}
			}
		}

	}
}
