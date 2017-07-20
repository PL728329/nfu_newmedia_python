today_in_history_4web
<br/>英文项目名称today_in_history_4web，today_in_history指历史上的今天，意在查询历史上今天所发生过的大事件。




# 简介 
回顾历史的长河，历史是生活的一面镜子：历史上的每一天，都是喜忧参半，历史是不能忘记的。查看历史上的今天发生的事情，增长见识。用户通过输入日期(1月1日-12月31日)，查询输入这一天在历史上发生的大事件(选取前五件事情)。数据来源于 [聚合数据](https://www.juhe.cn/)


		

## 输入：
用户输入日期（月、日）：上行输入月份，下行输入日期。在交互界面使用HTML5之[br标签](http://www.runoob.com/tags/tag-br.html)及[body标签]选日期元件(http://www.runoob.com/tags/tag-body.html)
## 输出：
用户得到输出结果为：历史上的某一天发生的大事件(选取前五件事情)，详见 [new_file.py](new_file.py)，使用for循环与切片
 
## 从输入到输出，本组作品使用了：
### 模块
* [request](http://www.python-requests.org/en/master/)  
* [Flask](http://www.pythondoc.com/flask/)

### 数据
* 来源：[聚合数据](https://www.juhe.cn/)
* 使用for循环与切片 
 



### API
* [聚合数据 历史上的今天](http://api.juheapi.com/japi/toh?key=4bc027ace0535ecf7e935870a1b9deef&v=1.0&month=11&day=1) 限量访问100次


## Web App动作描述

以下按web 请求（web request） - web 响应 时序说明

1. 後端伺服器启动：执行 today_in_history_4web.py  启动後端伺服器，等待web 请求。启动成功应出现：  * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)

2. 前端浏览器web 请求：访问 http://127.0.0.1:5000/ 启动前端web 请求

3. 後端伺服器web 响应：[ today_in_history_4web.py ](today_in_history_4web.py ) 中 执行 了@app.route('/') 下的 entry_page()函数，以HTML模版[templates/entry.html](templates/entry.html)    

4. 前端浏览器收到web 响应：出现HTML页面有HTML表单的输入 input 类型(type) 为"text"或"date"，变数名称(name)为'date'，[templates/entry.html](templates/entry.html)    

5. 前端浏览器web 请求：用户选取指标後按了提交钮「查询」，则产生新的web 请求，按照form元素中定义的method='POST' action='/content'，以POST为方法，动作为today_in_history_4web的web 请求

6. 後端服务器收到用户web 请求，匹配到@app.route('/content', methods=['POST'])的函数 weather_forecast()     

7. [today_in_history_4web.py ](today_in_history_4web.py ) 中 today_in_history_4web() 函数，把用户提交的数据，以flask 模块request.form['date']取到Web 请求中，HTML表单变数名称日期的值，使用flask模块render_template 函数以[templates/results.html](templates/results.html)模版为基础（输出）。

8. 前端浏览器收到web 响应：模版中[templates/results.html](templates/results.html) 的变数值正确的产生的话，前端浏览器会收到正确响应，显示
 信息



## 作者成员：
见[_team_.tsv](https://github.com/kkrrystal2/nfu_newmedia_python/blob/master/_team_.tsv)

