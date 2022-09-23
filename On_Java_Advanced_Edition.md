# On_Java_Advanced_Edition

## 01 枚举类型

### 1.2 在枚举类型中添加自定义方法

```java
package org.example;

public enum Run_RR {
    YANG("This is most helpful.."),
    QIAN("This is a good test of Enum"),
    TAO("This is a best chance for help poor boys..");

    private String description;

    private Run_RR(String description) {
        this.description = description;
    }

    public String getDescription(){
        return description;
    }
}
```

这么说，里面的`YANG` `QIAN` `TAO`这种类型其实也就是Run_RR的实例被，很像是一种递归调用的感觉。



**重载枚举类型中的方法**

```java
package org.example.enums;

import java.util.stream.Stream;

public enum SpaceShip {
    SCOUT, CARGO, TRANSPORT, CRUISER, BATTLESHIP, MOTHERSHIP;

    @Override
    public String toString() {
        String id = name();
        String lower = id.substring(1).toLowerCase();
        return id.charAt(0) + lower;
    }

    public static void main(String[] args) {
        Stream.of(values())
                .forEach(System.out::println);
    }
}
```

Enum 在编译器内部的类型就类似于这样

```java
enum Spring{
    TAO,
    THIN;
}

和这个 Enum<Spring> 是一样的。
```

**也可以用接口组织枚举。**
