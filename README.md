# 一、表结构

见附件

# 二、功能说明

## 2.1 系统登录页

> 系统登录页是用户访问受限资源或服务时首先接触到的界面，其设计旨在确保只有经过验证的用户才能访问敏感信息或执行特定操作。需要输入正确的用户名和密码才可登录成功。此系统默认管理员密码为 `admin/123456`

![image-20250320143523119](traffic_images/login.png)

前端代码

![image-20250323204822404](traffic_images/login_front1.png)

后端代码

![image-20250323204608799](traffic_images/login_back1.png)

## 2.2 系统首页

![image-20250323203050790](traffic_images/traffic_index.png)

前端代码

![image-20250323205026368](traffic_images/index_frontpng.png)

后端代码

![image-20250323204944360](traffic_images/index_back.png)

## 2.2 交通类型

> 拥有北京公共交通的基本类型，为后续路线提供服务，新增公交线路时需要选择该线路属于哪个公交类型。

- 市区普线: 覆盖城市主干道和密集居住区，班次密集（通常5-10分钟/班），满足日常短途出行需求（如买菜、上学、通勤接驳）。
- 郊区普线: 连接市区与近郊区域，班次间隔较长（20-40分钟），服务郊区居民进城通勤，可能绕行多个村镇。
- 快速公交: 专用封闭车道+智能信号优先，站台类似地铁（先购票后上车），实现“类地铁”速度，适合中长距离通勤走廊。
- 微循环线: 使用6-8米小型车辆，穿梭背街小巷，接驳地铁/公交枢纽与社区，解决“最后一公里”问题（如上海“社区巴士”）。
- 通勤线路: 定向服务职住分离群体，如大型居住区直达商务区，早高峰进城/晚高峰返程方向单向密集发车。
- 快速直达: 高峰时段运营，仅停靠大站/换乘枢纽，大幅缩短通勤时间（如北京“快专”线路）。
- 城际班线: 跨市域运营，连接邻近城市核心区域（如北京-廊坊班线），部分线路支持联程购票。
- 夜班线路: 22:00-次日5:00运营，覆盖娱乐场所集中区、医院、交通枢纽，部分线路与地铁末班车衔接。
- 商务班车: 企业/社区定制，点对点接送（如从大型住宅区直达科技园），采用舒适型车辆，可能配备WiFi。
- 远郊线路: 延伸至城市远郊或邻县，班次稀少（1-2小时/班），覆盖偏远地区，常作为城乡交通补充。
- 机场大巴: 专线连接市区与机场，提供行李舱，支持线上购票，班次与航班时刻匹配（如每30分钟一班）。
- 轨道交通: 虽未单独列出，但部分微循环/普线实际承担地铁/火车站接驳功能，需与轨道网络协同规划。
- 旅游集散: 连接交通枢纽与景区，提供套票/导游服务，旺季增开班次（如杭州“西湖环线”）。
- 通医专线: 北京部分医院曾开通“通医专线”，从回龙观、天通苑等大型社区直达积水潭医院、安贞医院等，早高峰单向发车，解决职住分离患者的就医难题。此类线路常与地铁、常规公交形成互补，构成“社区→医院”一站式网络。

![image-20250320143909970](traffic_images/traffic_type.png)

前端代码

![image-20250323205218089](traffic_images/type_front.png)

后端代码

![image-20250323205143274](traffic_images/type_back.png)

## 2.3 公共交通站点管理

> 站点有基础信息 名称、经纬度、状态等，根据经纬度可在地图上定位坐标📌

![image-20250320144604175](traffic_images/traffic_station.png)

前端代码

![image-20250323205357286](traffic_images/station_front.png)

后端代码

![image-20250323205330036](traffic_images/station_back.png)

## 2.4 公共交通路线管理

> 在线路信息列表中每一行都可点开查看该路线所经过的车站（可左右滑动）
>
> 在站点信息行下方有高德地图瓦片层进行地图展示，瓦片层上方有我们上方公交站点再此标注的位置信息。

注： 信息可能有误，需提前修改信息用于展示，例如5路。

![image-20250320144904468](traffic_images/traffic_route.png)

前端代码

![image-20250323205638727](traffic_images/route_front.png)

后端代码

![image-20250323205603684](traffic_images/route_back.png)

## 2.5 实时路线

> 用于搜索两地的出行路线信息。

![image-20250320145345584](traffic_images/traffic_real_route.png)

![image-20250323203157300](traffic_images/traffic_real_find.png)

前端代码

![image-20250323205710853](traffic_images/real_route_front.png)

后端代码

![image-20250323205507976](traffic_images/real_route_back.png)

## 2.6 在线购票

> 用于购买公共交通车票。

![image-20250320145520525](traffic_images/traffic_ticket_order.png)

![image-20250323203300848](traffic_images/traffic_buy1.png)

前端代码

![image-20250323205825222](traffic_images/buy_front.png)

后端代码

![image-20250323205858691](traffic_images/buy_back.png)

## 2.7 乘车出行

![image-20250323203352437](traffic_images/traffic_travel1.png)

![image-20250323203452099](traffic_images/traffic_go_zhifu.png)

前端代码

![image-20250323210019433](traffic_images/tranvel_front.png)

后端代码

![image-20250323210217795](traffic_images/travel_back.png)

## 2.8 意见反馈

![image-20250323203537335](traffic_images/traffic_feedback1.png)

![image-20250323203606177](traffic_images/traffic_feedback2.png)

前端代码

![image-20250323210328854](traffic_images/feed_front.png)

后端代码

![image-20250323210401725](traffic_images/feed_back.png)

## 2.9 用户管理

![image-20250320145750245](traffic_images/traffic_user.png)

前端代码

![image-20250323210435485](traffic_images/user_front.png)

后端代码

![image-20250323211627472](traffic_images/user_back.png)

## 2.10 角色管理

> 增删改查角色、给角色分配权限。给角色添加用户。

![image-20250320145833366](traffic_images/traffic_role.png)

前端代码

![image-20250323210502867](traffic_images/role_front.png)

后端代码

![image-20250323211557673](traffic_images/role_back.png)

## 2.11 权限管理

> 用户菜单权限功能。
>
> 演示系统功能时，最好在后台管理新增 /test。
>
> 因此处新增还需涉及代码层面的新增页面，请谨慎操作。

![image-20250320145920194](traffic_images/traffic_perm.png)

![image-20250320151330127](traffic_images/perm-add.png)

新增后还需去角色页面，给角色增加该页面的权限。

![image-20250320151507113](traffic_images/role_perm.png)

增加完成后刷新页面即可看到菜单下有此页面。

前端代码

![image-20250323210534185](traffic_images/perm_front.png)

后端代码

![image-20250323211520829](traffic_images/perm_back.png)

## 2.11 公告管理

> 用于维护系统公告信息，新增公告后用户进入系统可在首页看到公告信息(待实现)。

![image-20250320145959939](traffic_images/traffic_notice.png)

前端代码

![image-20250323211443387](traffic_images/notice_front.png)

后端代码

![image-20250323211417623](traffic_images/notice_back.png)

## 2.12 日志管理

> 记录系统重要操作记录，例如登录
>
> 本系统目前只记录登录，更多日志记录待后续追加。

![image-20250320150039791](traffic_images/traffic_logs.png)

前端代码

![image-20250323210604335](traffic_images/log_front.png)

后端代码

![image-20250323211336800](traffic_images/log_back1.png)

![image-20250323211303786](traffic_images/log_back2.png)

## 2.13 系统字典

> 系统字典，用户可点击右下角新增按钮增加字典分类名称
>
> 点击分类行右边的 `新增字典项` 的按钮，可为指定字典分类下增加字典项。
>
> 例：增加性别分类，性别分类下增加 男、女、未知

![image-20250320150128757](traffic_images/traffic_dict.png)

前端代码

![image-20250323210638706](traffic_images/dict_front.png)

后端代码

![image-20250323211226482](traffic_images/dict_back.png)

## 2.14 个人中心

> 个人中心用于修改用户基本信息，此系统目前只是修改用户昵称。

![image-20250320150224520](traffic_images/traffic_personcenter.png)

前端代码

![image-20250323210745734](traffic_images/profile_front.png)

后端代码

![image-20250323211052205](traffic_images/profile_back.png)

## 2.15 修改密码

> 鼠标悬浮右上角的头像，会出现修改密码的下拉选项，点击即可弹出密码修改框供用户修改密码。
>
> 修改成功后会直接退出系统重新登录。

![image-20250320150324150](traffic_images/traffic_repasswd.png)

前端代码

![image-20250323210817004](traffic_images/pass_front.png)

后端代码

![image-20250323210856287](traffic_images/pass_back.png)

# 附件

## 表结构
联系vx：tuoluoxueyuan
