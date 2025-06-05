本地项目链接：E:\研究生阶段\毕设\twitter_news\twitter_ai_papers
main是api运行的接口
服务器：10.10.12.36
路径：/home/auserwn/twitter_ai_papers
用户密码：
验证接口：http://10.10.12.36:8003/doc

--项目启动
# 切换用户
[root@localhost ~]# su - auserwn
# 进入项目
[auserwn@localhost ww-docgen-fastapi]$ cd /home/auserwn/twitter_ai_papers
创建虚拟环境python3 -m venv auserwn_ainews_venv
# 启动虚拟环境
[auserwn@localhost ww-docgen-fastapi]$ source auserwn_ainews_venv/bin/activate
# 启动项目接口
(auserwn_venv) [auserwn@localhost ww-docgen-fastapi]$ python3 main.py 
nohup python3 main.py > log.txt 2>&1 &
--------------------------------------------------------------------------------------------------------------------------------
(auserwn_ainews_venv) [auserwn@localhost twitter_ai_papers]$ export http_proxy="http://10.10.12.134:20172"
(auserwn_ainews_venv) [auserwn@localhost twitter_ai_papers]$ export https_proxy="https://10.10.12.134:20172"
# (auserwn_ainews_venv) [auserwn@localhost twitter_ai_papers]$ python3 t_1.py 

# 生成每天文件
(auserwn_ainews_venv) [auserwn@localhost twitter_ai_papers]$ python3 gen_daily_record.py 
-------------------------------------
http://10.10.12.36:8003/docs