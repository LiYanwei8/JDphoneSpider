#爬取京东手机前的准备工作
### 多线程爬取京东手机
IO密集型
京东手机数据
js数据加载
### 获取所有的手机
浏览器查看
https://search.jd.com/Search?keyword=%E6%89%8B%E6%9C%BA&enc=utf-8&qrst=1&rt=1&stop=1&vt=2&suggest=1.def.0.V00&wq=shouji&cid2=653&cid3=655&page=1&s=57&click=0
通过翻页得知page是通过1，3，5，...变化
range(1,10,2)
获取5页的手机信息

### 获取手机的详情页的url
通过浏览器查看
https://item.jd.com/4938580.html?jd_pop=6a706900-2d06-4bc9-886e-0712e3092eb3&abt=0
简化为https://item.jd.com/4938580.html

价格信息是Ajax更新的
通过火狐插件httpfox抓取价格请求
https://p.3.cn/prices/mgets?callback=jQuery9766052&type=1&area=1_72_2799_0&pdtk=&pduid=15006465310891261228802&pdpin=&pin=null&pdbp=0&skuIds=J_4938580&ext=11000000&source=item-pc
简化为
https://p.3.cn/prices/mgets?skuIds=J_4938580

