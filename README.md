# RedisService

## 依赖注入

```java
@Configuration
public class RedisConfig {

    @Autowired
    private StringRedisTemplate stringRedisTemplate;

    @Bean
    public RedisService redisService() {
        return new RedisServiceImpl(stringRedisTemplate);
    }

}
```

## 使用

```java
@Autowired
private RedisService redisService;
```

