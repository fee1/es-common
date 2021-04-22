# nacos cloud common
```text
    注册到nacos服务启动类
```
## @EnableAutoConfiguration
```text
    从classpath中搜索所有META-INF/spring.factories配置文件然后，将其中org.springframework.boot.autoconfigure.
EnableAutoConfiguration key对应的配置项加载到spring容器只有spring.boot.enableautoconfiguration为true（默认为true）的时候，才启用自动配置

    SpringFactoriesLoader 该类可以从classpath中搜索所有META-INF/spring.factories配置文件，并读取配置。
```
## @ConditionalOnProperty
```text
    控制配置类是否生效,可以使用@ConditionalOnProperty注解来控制@Configuration是否生效.
例：
    @ConditionalOnProperty(prefix="hello", value="enabled", matchIfMissing = true)//配置文件中 hello为前缀的，名字为ebable的值为true时生效
    @ConditionalOnProperty(prefix = "filter",name = "loginFilter",havingValue = "true")//prefix为配置文件中的前缀,name为配置的名字，havingValue是与配置的值对比值,当两个值相同返回true,配置类生效.
```
## @ConfigurationProperties
```text
    获取属性值
例：  
    @ConfigurationProperties(prefix = "hello") //获取属性值，前缀为hello为前缀的配置，后边值对应的属性的名称
```