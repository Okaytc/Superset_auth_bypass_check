# Superset_auth_bypass_check
Apahce-Superset身份认证绕过漏洞(CVE-2023-27524)检测工具

---

修复时间：2023.8.3
* 修复由于硬编码session时间过期导致的session失效，引用<a href="https://github.com/noraj/flask-session-cookie-manager">flask_session_cookie_manager</a>工具生成实时session进行检测。
* 修复由于未禁用重定向导致跳转/login/匹配状态码为200的bug

感谢nplookges师傅的反馈

---

开发环境：
python3

**避免python环境命名导致运行失败，可将python运行程序改为python3添加到环境变量中**

```python
使用方式（支持单个URL检测和批量检测）：//url做了合规处理，支持输入ip、ip:port样式

单个检测：python3 superset_auth_bypass_check.py -u

示例：python3 superset_auth_bypass_check.py -u http://192.168.1.1/

批量检测：python3 superset_auth_bypass_check.py -f

示例：python3 superset_auth_bypass_check.py -f url.txt

```

演示截图：

单个检测：
![图片](https://user-images.githubusercontent.com/50813688/234778920-e15d8736-580c-4c0d-9de1-a78a6ccc56b5.png)

批量检测：
![图片](https://user-images.githubusercontent.com/50813688/234778877-9d797ccd-b4b0-4e72-9dfa-0a90fbaafaac.png)

---

**免责声明**

**本工具仅用于教育和研究目的，以提高安全意识和改进软件开发实践。在使用本工具之前，请确保您遵守了相关法律法规和道德准则。使用之后，请删除此工具，使用者使用该工具出现任何非法攻击等违法行为，与作者无关。**
