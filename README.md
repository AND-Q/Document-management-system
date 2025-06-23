# 文档管理系统

## 项目介绍

本项目是一个基于SpringBoot和Vue开发的文档管理系统，旨在提供企业级文件存储、管理和共享解决方案。系统具备完善的用户权限控制、文件上传下载、文件分类管理等功能，适用于企业内部文档管理、团队协作等场景。

## 功能特点

- **文件管理**：支持文件上传、下载、预览、删除、批量操作等功能
- **用户管理**：完善的用户管理功能，支持用户注册、登录、信息修改等
- **角色管理**：基于RBAC的角色权限管理，可自定义不同角色的权限范围
- **菜单管理**：动态菜单配置，根据用户角色显示对应的功能菜单
- **权限控制**：基于JWT的身份验证和权限控制，保障系统安全
- **文件去重**：基于MD5的文件去重功能，节省存储空间
- **响应式设计**：适配不同设备的页面布局

## 技术架构

### 后端技术栈

- **SpringBoot 2.7.2**：基础框架
- **MyBatis-Plus 3.5.2**：ORM框架，简化数据库操作
- **MySQL**：关系型数据库
- **Hutool 5.8.5**：Java工具类库，提供丰富的工具方法
- **JWT**：基于Token的身份验证
- **Apache POI**：Excel导入导出功能

### 前端技术栈

- **Vue 2**：前端框架
- **ElementUI**：UI组件库
- **Axios**：HTTP客户端
- **Vue Router**：前端路由管理
- **Vuex**：状态管理

## 系统架构

系统采用前后端分离的架构设计：

- 前端：基于Vue的SPA应用，负责页面渲染和用户交互
- 后端：SpringBoot RESTful API，负责业务逻辑和数据处理
- 数据库：MySQL存储系统数据
- 文件存储：本地文件系统存储上传的文件

## 安装部署

### 环境要求

- JDK 1.8+
- Node.js 12+
- MySQL 5.7+
- Maven 3.6+

### 后端部署

1. 克隆项目到本地
```bash
git clone https://github.com/your-username/Document-management-system.git
```

2. 导入数据库
```bash
# 解压sql.zip文件，得到ems.sql
# 登录MySQL
mysql -u root -p
# 创建数据库
CREATE DATABASE vue;
# 导入SQL文件
use vue;
source path/to/ems.sql;
```

3. 修改配置文件
```yaml
# 修改 src/main/resources/application.yml 中的数据库连接信息和文件上传路径
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/vue?useUnicode=true&characterEncoding=utf8&useSSL=true
    username: root
    password: 你的密码

files:
  upload:
    path: 你的文件上传路径/
```

4. 使用IDEA打开项目并启动
```bash
# 或者使用Maven命令启动
mvn spring-boot:run
```

### 前端部署

1. 进入前端项目目录
```bash
cd vue
```

2. 安装依赖
```bash
npm install
```

3. 启动开发服务器
```bash
npm run serve
```

4. 构建生产环境代码
```bash
npm run build
```

## 访问系统

- 后端API：http://localhost:8082
- 前端页面：http://localhost:8080

## 默认账户

- 管理员账户：admin / 123456
- 普通用户：user / 123456

## 系统截图

### 系统主页
![系统主页](https://github.com/AND-Q/Document-management-system/blob/main/images/主页.png)

### 文件管理
![文件管理](https://github.com/AND-Q/Document-management-system/blob/main/images/文件管理.png)

### 用户管理
![用户管理](https://github.com/AND-Q/Document-management-system/blob/main/images/用户管理.png)

### 菜单管理
![菜单管理](https://github.com/AND-Q/Document-management-system/blob/main/images/菜单管理.png)

### 角色管理
![角色管理](https://github.com/AND-Q/Document-management-system/blob/main/images/角色管理.png)

## 开发指南

### 目录结构

```
├── src/                       # 源代码目录
│   ├── main/java/com/liu/springboot/
│   │   ├── common/            # 公共类
│   │   ├── config/            # 配置类
│   │   ├── controller/        # 控制器
│   │   ├── dto/               # 数据传输对象
│   │   ├── entity/            # 实体类
│   │   ├── exception/         # 异常处理
│   │   ├── mapper/            # MyBatis映射器
│   │   ├── service/           # 服务层
│   │   └── utils/             # 工具类
│   └── resources/             # 资源文件
├── vue/                       # 前端项目
└── sql.zip                    # 数据库脚本
```

## 贡献指南

1. Fork 本仓库
2. 创建您的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交您的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 打开一个 Pull Request

## 许可证

本项目采用 MIT 许可证 - 详情请参阅 [LICENSE](LICENSE) 文件

## 联系方式

如有任何问题或建议，请联系项目维护者。

---

感谢您使用文档管理系统！
