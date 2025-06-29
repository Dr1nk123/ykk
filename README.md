这是一个基于Selenium的教务系统题库自动化采集脚本，主要功能包括：

**核心功能**：
1. **浏览器自动化控制**
   - 使用setup_chrome函数配置Chrome无头浏览器
   - 支持本地Chrome和Chromedriver路径检测

2. **教务系统登录**
   - RSA加密密码处理
   - 多元素定位策略（ID/CLASS/XPATH）
   - 登录状态验证与自动重试

3. **智能题库抓取**
   - 多线程并发采集ThreadPoolExecutor
   - 题目去重机制（difflib相似度比对）
   - 自动翻页采集完整题库

4. **数据持久化**
   - JSON结构化存储
   - 生成可读的TXT版本
   - 根据测验ID自动创建文件

**技术亮点**：
- 通过user.env实现凭证隔离
- 异常处理机制（页面超时/元素丢失/网络中断）
- 浏览器指纹规避技术
- 自动生成登录页面快照（login_page.html）用于调试
        
**使用教程**：
- 加载requirements.txt中的python库
- 安装Chrome浏览器
- 通过user.env设置用户名及密码
- 更改quiz_scraper.py中的URL信息

参考文献https://blog.csdn.net/kobepaul123/article/details/128796839
        https://blog.csdn.net/xu_yong_lin/article/details/117521773，等等
