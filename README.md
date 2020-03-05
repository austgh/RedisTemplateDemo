# RedisTemplateDemo
stringRedisTemplate 连接redis
/**
 * StringRedisTemplate与RedisTemplate区别点
 * 两者的关系是StringRedisTemplate继承RedisTemplate。
 *
 * 两者的数据是不共通的；也就是说StringRedisTemplate只能管理StringRedisTemplate里面的数据，RedisTemplate只能管理RedisTemplate中的数据。
 *
 * 其实他们两者之间的区别主要在于他们使用的序列化类:
 * 　　　　RedisTemplate使用的是JdkSerializationRedisSerializer    存入数据会将数据先序列化成字节数组然后在存入Redis数据库。
 *
 * 　　 　  StringRedisTemplate使用的是StringRedisSerializer
 *
 * 使用时注意事项：
 * 　　　当你的redis数据库里面本来存的是字符串数据或者你要存取的数据就是字符串类型数据的时候，那么你就使用StringRedisTemplate即可。
 * 　　　但是如果你的数据是复杂的对象类型，而取出的时候又不想做任何的数据转换，直接从Redis里面取出一个对象，那么使用RedisTemplate是更好的选择。
 */
