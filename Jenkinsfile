//Pipeline para Windows
pipeline {
    agent any
        stages  {
            stage ('Backup e Att do Site') {
                steps {
                    //Backup
                    powershell 'copy C:/inetpub/wwwroot/app/* C:/Users/vagrant/Documents/bkp/app -recurse -ErrorAction SilentlyContinue'
                    //Atualização
                    powershell 'copy C:/data/jenkins_home/workspace/jenkins_file/* C:/inetpub/wwwroot/app/'
                }
            }

        }
} 

// Pipeline para Linux
//pipeline {
//    agent any
//        stages {
//            stage('Backup da pasta atual') {
//                steps { 
//                    sh 'cp -R /var/www/html/app /home/vagrant/bkp/backup_${BUILD_ID}'
//                }
//            }
//
//            stage('Atualização do index') {
//                steps {
//                    sh 'cp -R /var/lib/jenkins/workspace/Ambiente_Teste/* /var/www/html/app'
//                }
//            }
//
//            stage('Restart do Apache') {
//                steps {
//                    sh 'sudo systemctl restart apache2'
//                }
//            }
//        }
//}
