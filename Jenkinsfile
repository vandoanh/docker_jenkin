// node {
//     currentBuild.result = "SUCCESS"
//     try {
//         stage('Checkout'){
//             checkout scm
//         }

//         stage("Composer Update") {
//         // Run composer update
//             sh 'cd src && composer update'
//         }

//         stage("PHPUnit") {
//             // Run PHPUnit
//             sh 'cd src && ./vendor/bin/phpunit'
//         }
//         // Deploy to each branch
//         switch (env.BRANCH_NAME) {
//             case "master":
//                 stage("Build Docker"){
//                     sh 'rsync -avzhP --delete --exclude=.git/ --exclude=Jenkinsifle $WORKSPACE/ root@192.168.1.111:/root/docker/'
//                     //build docker & mount source to /var/www/html
//                     sh 'ssh root@192.168.1.111 "cd /root/docker/ && bash docker-compose.sh"'
//                     //push image to private dockerhub
//                     //....
//                 }
//                 break
//             case "develop":
//                 stage("Build Docker"){
//                     sh 'rsync -avzhP --delete --exclude=.git/ --exclude=Jenkinsifle $WORKSPACE/ root@192.168.1.112:/root/docker/'
//                     //build docker & mount source to /var/www/html
//                     sh 'ssh root@192.168.1.112 "cd /root/docker/ && bash docker-compose.sh"'
//                 }
//                 break
//             default:
//         // No deployments for other branches
//                 break
//         }
//     }
//     catch (err) {
//         currentBuild.result = "FAILURE"
//             mail body: "project build error is here: ${env.BUILD_URL}" ,
//             from: 'info@vnsys.wordpress.com',
//             replyTo: 'info@vnsys.wordpress.com',
//             subject: 'project build failed',
//             to: 'keepwalking86@vnsys.wordpress.com'
//         throw err
//     }    
// }