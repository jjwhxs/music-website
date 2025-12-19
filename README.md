### 系统介绍

基于SpringBoot和Vue实现的音乐网站采用前后端分离的架构方式，前台系统实现了用户注册/登录、首页、歌单、歌手、搜索、个人中心等功能模块，后台系统实现了系统首页、用户管理、歌手管理、歌单管理等功能模块。

### 技术选型

开发工具：idea2020.3+Webstorm2020.3

运行环境：jdk1.8+mysql5.7+nodejs14.21.3+redis5.0.9

服务端技术：springboot+mybatis-plus+data-redis+fastjson

前端技术：html+css+vue+axios+element-ui+echarts

### 成果展示

前台系统->注册/登录 输入图片说明

输入图片说明

前台系统->首页 输入图片说明

前台系统->歌单 输入图片说明

前台系统->歌手 输入图片说明

前台系统->个人中心 输入图片说明

后台系统->登录 输入图片说明

后台系统->系统首页 输入图片说明

后台系统->用户管理 输入图片说明

后台系统->歌手管理 输入图片说明

后台系统->歌单管理 输入图片说明

### 源码展示

@RestController

public class SingerController {

@Autowired

private SingerService singerService;

// 添加歌手

@PostMapping("/singer/add")

public R addSinger(@RequestBody SingerRequest addSingerRequest) {

    return singerService.addSinger(addSingerRequest);
    
}

// 删除歌手

@DeleteMapping("/singer/delete")

public R deleteSinger(@RequestParam int id) {

    return singerService.deleteSinger(id);
    
}

// 返回所有歌手

@GetMapping("/singer")

public R allSinger() {

    return singerService.allSinger();
    
}

// 根据歌手名查找歌手

@GetMapping("/singer/name/detail")

public R singerOfName(@RequestParam String name) {

    return singerService.singerOfName(name);
    
}

// 根据歌手性别查找歌手

@GetMapping("/singer/sex/detail")

public R singerOfSex(@RequestParam int sex) {

    return singerService.singerOfSex(sex);
    
}

// 更新歌手信息

@PostMapping("/singer/update")

public R updateSingerMsg(@RequestBody SingerRequest updateSingerRequest) {

    return singerService.updateSingerMsg(updateSingerRequest);
    
}

}

### 账号地址及其它说明

1、地址说明

前台系统：localhost:8080

后台系统：localhost:8081

2、账号说明

用户：shenghuo/123456

管理员：admin/123

3、目录结构展示

输入图片说明

4、项目结构展示

输入图片说明

5、运行步骤

1）创建数据库、导入sql脚本

2）修改application-dev.properties中的数据库配置文件，启动服务端

3）分别在music-client和music-manage目录下打开cmd，执行npm install下载依赖

4）下载完毕后启动前端npm run serve，访问端口

### 获取方式(可远程调试)

访问链接(在浏览器中手动输入下图中的地址)：

输入图片说明

若资源获取失败，可添加happy35596339(vx)或1204901965(qq)进行交流
