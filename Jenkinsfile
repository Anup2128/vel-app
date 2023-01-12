pipeline{
	agent any
	
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
			sh " cp -r index.html /var/www/html"	
			}
		}
		
		stage('permission-to-index'){
			steps{
				sh " chmod -R 777 * /var/www/html/index.html
			}
		}
	}
}
