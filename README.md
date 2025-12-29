### 系统介绍

基于SpringBoot和Vue实现的音乐网站采用前后端分离的架构方式，前台系统实现了用户注册/登录、首页、歌单、歌手、搜索、个人中心等功能模块，后台系统实现了系统首页、用户管理、歌手管理、歌单管理等功能模块。

### 技术选型

开发工具：idea2020.3+Webstorm2020.3

运行环境：jdk1.8+mysql5.7+nodejs14.21.3+redis5.0.9

服务端技术：springboot+mybatis-plus+data-redis+fastjson

前端技术：html+css+vue+axios+element-ui+echarts

### 成果展示

前台系统->注册/登录
<img width="1882" height="881" alt="前台系统-登录" src="https://github.com/user-attachments/assets/498d0d2b-c213-450b-8a09-69bcd26b621e" />

<img width="1876" height="881" alt="前台系统-注册" src="https://github.com/user-attachments/assets/0b862e59-7b9f-409d-b85e-032966df0367" />

前台系统->首页
<img width="1880" height="1032" alt="前台系统-首页" src="https://github.com/user-attachments/assets/66cf401e-75ab-4415-91b8-18aac6ddc2c8" />

前台系统->歌单
<img width="1879" height="1034" alt="前台系统-歌单" src="https://github.com/user-attachments/assets/da717077-985b-471a-9bde-99c97b2f3ea4" />

前台系统->歌手
<img width="1881" height="1032" alt="前台系统-歌手" src="https://github.com/user-attachments/assets/3c494f8d-d378-4705-8651-a1ab87df462d" />

前台系统->个人中心
<img width="1900" height="881" alt="前台系统-个人中心" src="https://github.com/user-attachments/assets/058870d1-877b-4296-ac0e-ee7ea7b040b2" />

后台系统->登录
<img width="1890" height="1034" alt="后台系统-登录" src="https://github.com/user-attachments/assets/50bb92d5-01ca-4e25-8360-84f5171b87af" />

后台系统->系统首页
<img width="1885" height="1035" alt="后台系统-系统首页" src="https://github.com/user-attachments/assets/ef3de282-2e42-4a6e-817e-de06e9471739" />

后台系统->用户管理
<img width="1889" height="1032" alt="后台系统-用户管理" src="https://github.com/user-attachments/assets/789e7450-d5fd-4e02-b627-868c0960ab38" />

后台系统->歌手管理
<img width="1890" height="1031" alt="后台系统-歌手管理" src="https://github.com/user-attachments/assets/7d58fe1d-8325-4713-acc0-ef41717b1413" />

后台系统->歌单管理
<img width="1890" height="1032" alt="后台系统-歌单管理" src="https://github.com/user-attachments/assets/a2a2d9ee-bb02-40d4-a885-e2098f22bc9b" />

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

<img width="1109" height="179" alt="目录结构展示" src="https://github.com/user-attachments/assets/1487bdaf-9f46-4aa6-8bda-340b380c0778" />

4、项目结构展示

<img width="1691" height="945" alt="项目结构展示" src="https://github.com/user-attachments/assets/4cc62d0f-d6b8-45bc-a282-428f4e970ffa" />

5、运行步骤

1）创建数据库、导入sql脚本

2）修改application-dev.properties中的数据库配置文件，启动服务端

3）分别在music-client和music-manage目录下打开cmd，执行npm install下载依赖

4）下载完毕后启动前端npm run serve，访问端口

### 获取方式(可远程调试)

访问链接(在浏览器中手动输入下图中的地址)：

<img width="1125" height="128" alt="链接" src="https://github.com/user-attachments/assets/70954dc7-8527-443b-9d9f-25ce878af168" />

若资源获取失败，可添加happy35596339(vx)或2061772307(qq)进行交流
