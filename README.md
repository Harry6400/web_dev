# Web Base

这是一个用于学习 Java Web 基础流程的练习项目。仓库以一个最小 Servlet 应用串起 Maven 构建、Tomcat 运行、静态首页和 Servlet 请求处理，适合作为 Web 开发课程早期阶段的实验记录。

## 项目用途

- 熟悉 Maven Web 项目的基础目录结构。
- 观察 `index.html`、`web.xml` 与 Servlet 映射之间的关系。
- 通过 `HelloServlet` 练习后端请求处理与动态响应输出。

当前仓库以学习和验证基础配置为主，不是完整业务系统。

## 技术栈

- Java 21
- Servlet API 4.0.1
- Maven
- Tomcat Maven Plugin

## 目录说明

```text
.
|-- pom.xml
|-- src/main/java/com/example/servlet/HelloServlet.java
|-- src/main/webapp/index.html
|-- src/main/webapp/WEB-INF/web.xml
|-- lib/servlet-api.jar
`-- PROJECT.md
```

`PROJECT.md` 记录了更完整的创建过程、学习进度、常见问题和后续学习规划。

## 运行方式

```bash
mvn tomcat7:run
```

启动后可访问：

- 首页：`http://localhost:8080/web_base/`
- Servlet 页面：`http://localhost:8080/web_base/hello`

## 当前状态

- 已完成基础 Servlet 示例、部署描述符和 Maven 运行配置。
- `lib/servlet-api.jar` 是早期学习阶段保留的本地依赖痕迹；项目依赖以 `pom.xml` 为准。
