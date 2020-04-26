# Heroku aria2

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## 无需服务器即可离线下载并自动上传到OneDrive
## 详细教程在 [https://aroins.com/67](https://aroins.com/67)

1. 使用Rclone将OneDrive挂载到本地计算机
2. 打开 `C:\Users\Administrator\.config\rclone\rclone.conf`文件：

```conf
[DRIVENAME]
type = 
token = 
drive_id = 
drive_type = 

```

3. 找到`type =`到`drive_type = `内容，每一行后面加上`\n`如：
```conf
type =  xxx \n
token = {xxx} \n
drive_id = xxx \n
drive_type = xxx \n
```
4. 将四行内容全部复制粘贴到 `RCLONE_CONFIG`
6. 设置 `RCLONE_DESTINATION` 为OneDrive网盘上传路径，如：`/update`
