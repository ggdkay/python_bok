## configParser

解析文件.ini

```
[tomcat_server] 
Ip_address:192.168.22.10 
account: testerhome 
password: 123456

[mail_server]
smtp_host:smtp.126.com 
from_address:no-replay_autotest@126.com 
to_address: testerhome@126.com
```

```
Config实例常用方法:
• config.get(‘Section’, ‘options’) : 获取指定section下对应
option的值
• config.sections(): 获取配置文件中所有的sections
• config.has_section(‘secion’): 判断配置文件中是否有对应
session
• config.has_option(‘section’, ‘option’): 判断对应section是否
有对应的option
```

## 场景

```
import ConfigParser
config = ConfigParser.ConfigParser()
cfg = config.read(file)
cfg.get('tomcat_server','password')

```



