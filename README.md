# repository

maven repository

# 插件仓库配置示例

```xml

<project>
    <build>
        <plugins>
            <!-- https://github.com/xiangqians/defoliation-maven-plugin -->
            <plugin>
                <groupId>org.xiangqian</groupId>
                <artifactId>defoliation-maven-plugin</artifactId>
                <version>2022.4</version>
                <executions>
                    <execution>
                        <id>properties</id>
                        <phase>validate</phase>
                        <goals>
                            <goal>properties</goal>
                        </goals>
                        <configuration>
                            <includes>
                                <include>${project.basedir}/src/main/resources/bootstrap.yml</include>
                            </includes>
                            <properties>
                                <server.port>server.port</server.port>
                            </properties>
                            <skip>true</skip>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>

    <pluginRepositories>
        <!-- github -->
        <pluginRepository>
            <id>github</id>
            <url>https://raw.githubusercontent.com/xiangqians/repository/master/maven</url>
        </pluginRepository>
    </pluginRepositories>
</project>
```

如果出现异常：  
Could not transfer artifact org.xiangqian:defoliation-maven-plugin:pom:2022.4 from/to
github (https://raw.githubusercontent.com/xiangqians/repository/master/maven): 请求的名称有效，但是找不到请求的类型的数据。 (
raw.githubusercontent.com)

可以尝试这么解决：

1. 通过IP查询工具查询 ```raw.githubusercontent.com``` 域名对应IP
2. 在本机做域名映射

# 仓库配置示例

```mxl

```

