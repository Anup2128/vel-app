pipeline{
	agent{
		label{
			label'built-in'
			customWorkspace'/mnt/deploy'
		}
	}
	
	stages{
		stage('install-httpd'){
			steps{
				sh " yum install httpd -y"
			}
		}
		
		stage('start-httpd'){
			steps{
				sh " service httpd start"
			}
		}
		
		stage('deply-index'){
			steps{
			sh " cp -r /mnt/deploy/index.html /var/www/html"	
			}
		}
		
		stage('permission-to-index'){
			steps{
				sh " chmod -R 777 * /var/www/html/index.html"
			}
		}
	}
}
