# aop
spring aop底层实现有两种方法：一种是基于JDK动态代理；另一种是基于CGLib动态代理。
JDK动态代理通过接口来实现方法拦截，所以必须确保要拦截的目标方法在接口中有定义，否则无法实现拦截。

CGLib动态代理中通过动态代理生成代理子类来实现方法拦截，所以必须确保要拦截的目标方法被子类访问，也就是目标方法必须定义为非final以及非私有实例方法。

1.spring aop和jdk动态代理、CGLib、asm的关系
asm是轻量级的字节码处理框架，因为java的反射机制无法获取入参名，spring就利用asm处理@AspectJ中所描述的方法入参名。
