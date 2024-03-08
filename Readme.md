# 烤肠-API-SDK

# **烤肠-API 接口分享平台开发者工具包**

### 快速开始 🚀

**要开始使用 烤肠-API-SDK，您需要按照以下简单进行操作:**



1. #### **下载SDK工具包并导入项目**

2. #### 前往 [烤肠-API 接口分享平台](https://api.kaochang.me/) 获取开发者密钥对

3. #### 初始化客户端 KaochangClient 对象

- 方法 1 ：主动实例化客户端

  ```java
  String accessKey = "你的 accessKey";
  String secretKey = "你的 secretKey";
  KaochangClient client = new KaochangClient(accessKey, secretKey);
  ```

- 方法 2 ：通过配置文件注入对象

  - yml

    ```yml
    # 烤肠-API 配置
    kaochang:
      client:
        access-key: 你的 accessKey
        secret-key: 你的 secretKey
    ```

 - properties
  
    ```properties
    kaochang.client.access-key=你的 accessKey
    kaochang.client.secret-key=你的 secretKey
    ```

#### 4. 使用API服务

   ```java
    @Resource
    private KaochangClient client;
   ```

#### 5. 发起请求示例

示例：随机毒鸡汤

- 示例一 ：**通过配置文件配置后自动注入 推荐👍**

```java
String res = kaochangClient.yanInterface("utf-8", "json");
System.out.println("res = " + res);
```

- 示例二 ：主动注入
```java
KaochangClient client = new KaochangClient("你的 accessKey", "你的 secretKey");
String res = kaochangClient.yanInterface("utf-8", "json");
System.out.println("res = " + res);
```

响应示例：

```json
{
    "code": 0,
    "data": {
        "text": "现在不努力，以后别人壁咚的墙，都是你搬的砖。"
    },
    "message": "ok"
}
```

