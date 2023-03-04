# 简介

maven repository

# 插件仓库配置示例

```xml

<project>
    <build>

        <plugins>

            <!-- https://github.com/xiangqians/maven-tool-plugin -->
            <plugin>
                <groupId>org.xiangqian</groupId>
                <artifactId>maven-tool-plugin</artifactId>
                <version>2022.4</version>
                <executions>
                    <execution>
                        <id>uuid</id>
                        <phase>validate</phase>
                        <goals>
                            <goal>uuid-gen</goal>
                        </goals>
                        <configuration>
                            <name>uuid</name>
                            <hyphen>false</hyphen>
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
github (https://raw.githubusercontent.com/xiangqians/repository/master/repository): 请求的名称有效，但是找不到请求的类型的数据。 (
raw.githubusercontent.com)

可以尝试这么解决：

1. 通过IP查询工具查询 ```raw.githubusercontent.com``` 域名对应IP
2. 在本机做域名映射

