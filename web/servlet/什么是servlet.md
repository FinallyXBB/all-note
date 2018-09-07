# 什么是Servlet
Servlet是JavaWeb的三大组件之一，它属于动态资源。Servlet的作用是处理请求，服务器会把接收到的请求交给Servlet来处理，在Servlet中通常需要：
* 接收请求数据；
* 处理请求；
* 完成响应。
例如客户端发出登录请求，或者输出注册请求，这些请求都应该由Servlet来完成处理！Servlet需要我们自己来编写，每个Servlet必须实现`javax.servlet.Servlet`接口。

# 实现Servlet的方式
实现Servlet有三种方式：
* 实现`javax.servlet.Servlet`接口；
* 继承`javax.servlet.GenericServlet`类；
* 继承`javax.servlet.http.HttpServlet`类；
通常我们会去继承HttpServlet类来完成我们的Servlet，但学习Servlet还要从`javax.servlet.Servlet`接口开始学习。
```java
public interface Servlet {
  public void init(ServletConfig config) throws ServletException;
  public ServletConfig getServletConfig();
  public void service(ServletRequest req, ServletResponse res)
      throws ServletException, IOException;
  public String getServletInfo();
  public void destroy();
}
```
