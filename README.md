# risc-v_dev
基于docker ubuntu 20.04版本的 RISC-V 交叉编译环境

## 1. 构建docker image
在当前目录执行：

> ./scripts/build.sh

会创建名称为 **${USERNAME}/risc-v-u:latest** 的docker image  
例如：用户alice创建的默认image名称为 alice/risc-v-u:latest


## 2. 安装脚本

构建完毕后，在当前目录执行：

> ./scripts/install.sh [TargetPath]

**TargetPath** 的默认值为： `${HOME}/.local`  
如不指定**TargetPath**，则生成的脚本为：`${HOME}/.local/docker_env/bash_risc-v-u_env`  

## 3. 使用方法
对于用户alice, 参考安装脚本提示：
<pre>First, exec:
    source /home/alice/.local/docker_env/bash_risc-v-u_env
Then, use:
    [ENTRY=&lt;entry&gt;] docker_bash [arg1]...</pre>



如需永久生效，可将
>source /home/alice/.local/docker_env/bash_risc-v-u_env

添加到${HOME}/.bashrc
