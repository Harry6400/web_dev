# Web Base 项目文档

## 项目创建目的
本项目是一个基础的Web应用，用于学习Web全栈开发。通过这个项目，可以掌握Java Web开发的基本概念和流程，包括Servlet开发、Tomcat服务器配置、Maven构建等知识。

## 技术栈
- **后端**: Java 21
- **Web框架**: Servlet API 4.0.1
- **构建工具**: Maven 3.x
- **服务器**: Apache Tomcat 7.0.47 (通过maven-tomcat7-plugin运行)
- **IDE**: IntelliJ IDEA Ultimate / Trae

## 项目结构及功能说明

### 项目文件结构详解
```
web_base/
├── .idea/              # IntelliJ IDEA配置文件目录
├── .vscode/            # VS Code配置文件目录
├── lib/                # 本地依赖库（已弃用，改用Maven管理）
│   └── servlet-api.jar
├── src/                # 源代码主目录
│   └── main/
│       ├── java/       # Java后端代码目录
│       │   └── com/example/servlet/
│       │       └── HelloServlet.java  # Servlet控制器
│       └── webapp/     # Web前端资源目录
│           ├── WEB-INF/
│           │   └── web.xml  # Web应用部署描述符
│           └── index.html   # 网站首页（前端页面）
├── target/             # Maven构建输出目录
├── pom.xml             # Maven项目配置文件
└── web_base.iml        # IDEA模块配置文件
```

### 各文件夹的作用详解

#### 前端部分（webapp目录）
- **index.html**: 网站的静态首页，包含HTML结构，是用户访问网站时看到的第一个页面
- **webapp/WEB-INF/web.xml**: Web应用的配置文件，定义Servlet映射、欢迎页面等

#### 后端部分（java目录）
- **HelloServlet.java**: Servlet控制器，处理HTTP请求，生成动态内容（如当前时间）

#### 构建工具（Maven）
- **pom.xml**: Maven配置文件，管理项目依赖、构建配置和插件

## 项目创建过程
1. **创建项目目录结构**：使用Maven标准目录结构
2. **编写Servlet代码**：创建HelloServlet类，实现动态页面生成
3. **配置web.xml**：配置Servlet映射和欢迎页面
4. **编写HTML页面**：创建index.html作为首页
5. **配置pom.xml**：添加Servlet依赖和Tomcat插件
6. **构建项目**：使用Maven构建WAR文件
7. **部署运行**：使用maven-tomcat7-plugin启动Tomcat服务器

## 运行环境
- **操作系统**: Windows 10/11
- **Java版本**: JDK 21
- **Maven版本**: 3.x
- **Tomcat版本**: 7.0.47 (通过maven-tomcat7-plugin)

## 运行项目

### 启动服务器
```bash
mvn tomcat7:run
```

### 访问网站
- **首页**: http://localhost:8080/web_base/
- **Servlet页面**: http://localhost:8080/web_base/hello

### 关闭服务器
- 在终端中按 `Ctrl + C`
- 或执行 `taskkill /F /IM java.exe`

## 学习内容进度表

| 类别 | 技术/知识点 | 状态 | 学习阶段 | 应用场景 |
|------|-------------|------|----------|----------|
| **前端基础** | HTML基础 | ✅ 已学习 | 基础 | 构建网页结构 |
| **前端基础** | CSS样式 | ⏳ 待学习 | 进阶 | 美化页面外观 |
| **前端基础** | JavaScript | ⏳ 待学习 | 进阶 | 实现交互功能 |
| **前端组件** | 下拉框(select) | ⏳ 待学习 | 进阶 | 表单选择功能 |
| **前端组件** | 按钮(button) | ⏳ 待学习 | 进阶 | 用户交互操作 |
| **前端组件** | 表格(table) | ⏳ 待学习 | 进阶 | 数据展示 |
| **前端框架** | Bootstrap | ⏳ 待学习 | 高级 | 快速开发响应式页面 |
| **前端框架** | Vue.js | ⏳ 待学习 | 高级 | 构建单页应用 |
| **后端基础** | Servlet API | ✅ 已学习 | 基础 | 处理HTTP请求 |
| **后端基础** | JSP | ⏳ 待学习 | 进阶 | 动态页面生成 |
| **后端框架** | Spring MVC | ⏳ 待学习 | 高级 | 企业级Web开发 |
| **数据库** | MySQL | ⏳ 待学习 | 进阶 | 数据存储和查询 |
| **数据库框架** | MyBatis | ⏳ 待学习 | 高级 | ORM框架 |
| **服务器** | Tomcat配置 | ✅ 已学习 | 基础 | Web应用部署 |
| **构建工具** | Maven | ✅ 已学习 | 基础 | 项目构建和依赖管理 |

## 项目发展规划

### 近期目标（1-2周）
1. **丰富前端页面**
   - 添加CSS样式美化页面
   - 学习JavaScript基础
   - 实现下拉框、按钮等交互组件

2. **扩展Servlet功能**
   - 添加表单处理功能
   - 实现简单的数据处理逻辑

### 中期目标（1个月）
1. **引入前端框架**
   - 学习Bootstrap快速构建美观页面
   - 添加响应式设计支持移动端

2. **添加数据库支持**
   - 集成MySQL数据库
   - 创建数据模型和DAO层

### 长期目标（持续学习）
1. **学习企业级框架**
   - Spring MVC框架学习
   - MyBatis ORM框架学习
   - Vue.js前端框架学习

2. **构建完整应用**
   - 实现用户登录注册功能
   - 开发数据管理系统
   - 学习RESTful API开发

## 遇到的问题及解决方法

### 问题1：Tomcat启动失败 - JAVA_HOME环境变量未设置
**问题描述**：启动Tomcat时提示"Neither the JAVA_HOME nor the JRE_HOME environment variable is defined"
**解决方法**：
- 设置JAVA_HOME环境变量指向JDK安装目录
- 临时解决方案：在命令行中执行`set JAVA_HOME=D:\JDK21`

### 问题2：端口8080被占用
**问题描述**：启动Tomcat时提示"Address already in use: bind <null>:8080"
**解决方法**：
- 查找占用端口的进程：`netstat -ano | findstr :8080`
- 终止占用端口的进程：`taskkill /F /PID [进程ID]`

### 问题3：Java版本不匹配警告
**问题描述**：项目配置Java 1.8但实际运行环境是Java 21
**解决方法**：
- 修改pom.xml中的Java版本配置，将`maven.compiler.source`和`maven.compiler.target`从1.8改为21

### 问题4：构建失败 - 文件被占用
**问题描述**：执行`mvn clean package`时提示无法删除文件
**解决方法**：
- 停止所有Java进程：`taskkill /F /IM java.exe`
- 重新执行构建命令

## 维护记录
- **2026-03-26**: 创建项目，实现基本Servlet功能
- **2026-04-02**: 更新项目文档，添加学习内容表格和项目发展规划

---

*注：本文件将随着项目的扩展不断更新维护。*