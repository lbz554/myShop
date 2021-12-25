# myShop
华南理工大学java web购物网站实现
姓名：刘保柱
学号：201930342301
Src:
·Filter
----CharacterFilter对每一个处理请求的servlet，设置请求与相应的文本编码为utf-8，对请求的每个参数统一为utf-8编码
----SQLFilter对每个需要与数据库交互的servlet设置JDBC连接

·Servlets.car
----addToCar处理前端post来的商品信息，对session中的car元素（ArrayList<Object[]>）的进行处理，添加购物车
----DeleteInCar处理前端post来的商品信息，对session中的car元素（ArrayList<Object[]>）的进行处理，删除购物车

·Servlet.Customers
----CustomerLoginServlet与数据库确认是否登录成功，成功则进入商品界面，否则返回用户登录界面
----GoodsToCustomers读取数据库goods表的所有内容，并转发给前端
----SearchServlet读取数据库goods表的符合搜索关键词（searchText）内容，并转发给前端
·servlets.goods
----GoodsAdd处理前端post请求，对数据库goods表增加商品
----GoodsChange处理前端post请求，对数据库goods表修改商品
·servlets.users
----showUserListServlet对管理员展示已注册的用户信息
----UserLoginServlet对用户输入信息进行校对，登录
----UserRegisterServlet用户注册信息，与数据库进行交互

WebCotent：
·Customer
----buyClear支付购物车的所有物品后发邮件，登记用户行为日志（购买）
----car读取session.car展示购物车
----clearCar清空Session.car转发到car.jsp
----goodsInfo商品详细信息展示界面，登记用户行为日志（浏览）
----pay付款界面，展示付款码，计算总支付金额
----search搜索结果界面展示
----showForBuy购买商品界面展示
----userLogin用户登录界面
·IMG
商品图片源文件
·My_QR_Code付款码
·Sale
----addGoods管理员增加商品
----goodsChange管理员修改商品信息
----log用户行为日志
----saleIndex管理员行为界面
----showForSale管理员管理商品界面
----userInfo用户信息界面
----userLogin管理员登录界面
·WEB-INF
----lib web.xml配置文件

Index.jsp商店操作索引界面
userRegister用户注册界面
