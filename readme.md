
###测试目的
检验使用`docker -v`将宿主机文件挂载到docker容器某`dir`下配置文件时，是否会对`dir`目录下其他配置文件产生影响（覆盖）
###过程

系统环境:  `Ubuntu 16.04`  
docker版本:  `docker-ce-18.03.1` 
测试镜像:  `tomcat:8.0.53-jre8`

文件挂载前启动容器检查文件目录：
![1](u-ce-before.png)
挂载后检查主机和容器目录：
![2](u-ce-after.png)

系统环境： `Ubuntu 16.04`
docker版本： `18.03.1-ee-1`
测试镜像：`tomcat:8.0.53-jre8`
文件挂载前启动容器检查文件目录：
![3](u-ee-before.png)
挂载后检查主机和容器目录：
![4](u-ee-after.png)

系统环境：`Red Hat Enterprise Linux Server release 7.2` 
docker版本： `17.06.1-ee-2` 
测试镜像：`nginx:stable`
文件挂载前启动容器检查文件目录：
![5](r-ee-before.png)
挂载后检查主机和容器目录：
![6](u-ee-after.png)

###结论
将宿主机文件挂载到镜像容器的文件中，不会覆盖容器镜像中的其他文件
