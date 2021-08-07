## Maven

### 发布jar到maven私服命令

mvn deploy:deploy-file -Dmaven.test.skip=true -Dfile=C:\Users\HUANGYIXIN\Desktop\datax\postgresqlwriter-0.0.1-SNAPSHOT.jar -DgroupId=com.alibaba.datax -DartifactId=postgresqlwriter -Dversion=0.0.1-SNAPSHOT -Dpackaging=jar -DrepositoryId=snapshots -Durl=http://xxx/repository/maven-snapshots/