currentBuild.displayName = "Final_Demo # "+currentBuild.number
	def getDockerTag(){
        def tag = sh script: 'git rev-parse HEAD', returnStdout: true
			return tag
		}
node('master'){
	
		
		environment{
	    Docker_tag = getDockerTag()
        }
		
		stage('ansible playbook'){
			
			 	script{
				    sh '''final_tag=$(echo $Docker_tag | tr -d ' ')
				     echo ${final_tag}test
				     echo $final_tag'''
				}
		
		}
	}
