#!/bin/sh
# 检查是否已经安装过，避免重复执行
if [ ! -f /etc/my_ipk_installed ]; then
    # 强制安装本地 ipk（--force-depends 可以忽略依赖报错，但最好确保依赖已内置）
    opkg install /root/runner.ipk --force-depends

    # 安装后标记并删除安装包释放空间
    touch /etc/my_ipk_installed
    rm /root/runner.ipk
fi
