# RSAUtils
RSA简单加密工具

### 使用方法：

> 在Android Studio的Project build.gradle中加入：

    allprojects {
        repositories {
            maven { url 'https://jitpack.io' }
        }
    }

> 在Module build.gradle中添加依赖：

    implementation 'com.github.LanceShu:rsa-util:1.2'

### 代码使用：

##### 获取RSAUtils的单例对象：

    RSAUtils rsaUtils = RSAUtils.getInstance();

##### 使用RSAUtils对象的公钥对明文进行加密，公钥为rsaUtils.getPubKey()：

    String encodeMsg = rsaUtils.encodeMessage(msg, rsaUtils.getPubKey());

##### 使用RSAUtils对象的私钥对密文进行解密，私钥为rsaUtils.getPriKey()：

    msg = rsaUtils.decodeMessage(encodeMsg, rsaUtils.getPriKey());

### RSA原理：

[RSA算法原理（一）](http://www.ruanyifeng.com/blog/2013/06/rsa_algorithm_part_one.html)

[RSA算法原理（二）](http://www.ruanyifeng.com/blog/2013/07/rsa_algorithm_part_two.html)