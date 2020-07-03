# Sensirion
## 遇到的问题及解决方法
1.权限问题
winSCP上传文件到服务器失败，提示permission denied，返回码3
方法链接：https://blog.csdn.net/whosyourdaddy10086/article/details/80340549?tdsourcetag=s_pctim_aiomsg
发现以上链接提供的方法并没有解决问题，之后使用超级用户登录代替普通用户成功解决了问题
方法链接：https://blog.csdn.net/c__try/article/details/88884047

2.自动执行
通过在树莓派LX终端输入指令sudo crontab -e后选择方式[2]进行编辑
将下列代码写入最后，并保存退出
*/1 * * * * python /home/pi/dht11/tmp.py

*/1 * * * * python /home/pi/dht11/hum.py

*/1 * * * * python /home/pi/dht11/wendu.py


