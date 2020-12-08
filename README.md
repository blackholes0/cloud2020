# cloud2020
springcloud全家桶练习

软件架构
springcloud最新
2020年3月6日 重构时注意将lombok依赖复制到api-commons下时要注意删除optional选项，否则当该选项为true时，说明该依赖禁止依赖传递，则依赖api的模块不会依赖lombok。

        <!--    错误      -->
          <dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
          </dependency>
          <!--    正确      -->
           <dependency>
              <groupId>org.projectlombok</groupId>
              <artifactId>lombok</artifactId>
           </dependency>
           
Eureka注册中心集群环境: 负载均衡，容错控制

Eureka集群搭建

1、修改hosts
  C:\Windows\System32\drivers\etc 
  127.0.0.1 eureka7001.com
  127.0.0.1 eureka7002.com
