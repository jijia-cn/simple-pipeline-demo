node {
    sh 'echo hello world'
	
	//定义mvn环境
    def mvnHome = 'tool M3'
    env.PATH = "${mvnHome}/bin:${env.PATH}"

    stage('mvn test'){
        //mvn 测试
        sh "mvn test"
    }

    stage('mvn build'){
        //mvn构建
        sh "mvn clean install -Dmaven.test.skip=true"
    }

    stage('deploy'){
        //执行部署脚本
        echo "deploy ......" 
    }
}