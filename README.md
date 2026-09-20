# javaweb学习项目


前后端分离的企业员工管理系统，包含提供 RESTful 接口的后端服务与管理端 Web 后台。

### 技术栈

**后端**：Java 17、Spring Boot、Spring MVC、MyBatis、MySQL、PageHelper、Lombok、Logback

**鉴权与增强**：JWT（jjwt）、Servlet Filter 拦截、ThreadLocal 上下文传递、AOP 环绕通知、自定义注解

**管理端**：Vue 3、Element Plus、Vue Router、Pinia、Axios、ECharts、Vite

**部署**：Nginx 静态资源托管 + API 反向代理

### 功能

**部门管理**：列表查询、新增、修改、按 ID 查询、删除

**员工管理**：分页查询，支持按姓名模糊匹配、性别、入职日期区间组合筛选，关联查询所属部门名称

**登录鉴权**：JWT 令牌签发与校验；TokenFilter 统一拦截，放行登录请求，令牌缺失或解析失败返回 401，解析出的员工 ID 存入 ThreadLocal 供后续使用

**操作日志**：自定义 `@LogOperation` 注解 + AOP 环绕通知，记录操作人、类名、方法名、参数、返回值与耗时

**统一响应**：`Result` / `PageResult` 统一封装返回结构
