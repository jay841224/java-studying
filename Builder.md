# Builder 以車子為例
當一個複雜構造，在建構時有大量變數和對象需要進行初始化。在初始化過程甚至需要使用眾多構造函數。

![null](https://github.com/jay841224/java-studying/blob/main/src/problem2.png?raw=true)

---
## 大致結構
![null](https://github.com/jay841224/java-studying/blob/main/src/builder%E7%B5%90%E6%A7%8B.png?raw=true)

### builder
#### interface Builder:
* 定義每台車要實作的方法。
* 讓不同車型去 implement。
---
### director:
固定型號之車輛。
* 客戶可以選擇以定義好的型號，或是自定義自己的車子。
---
### car builder:
實作車子。
---
### car manual builder:
用來介紹車子各個功能。

---
## Builder 生成器適用場合
1. Builder 建造模式可以避免建構子的多載(Overload)。
```java
class Pizza {
    Pizza(int size) {}
    Pizza(int size, boolean cheese) {}
    Pizza(int size, boolean cheese, boolean pepperoni) {}
}
```
面對不同客戶的要求，需要建造多種建構子，造成程式碼不易閱讀，用 Builder 生成器可以壁面這樣的情況。Builder 生成器使我們可以分步驟生成對象。

2. 希望用代碼生成不同形式產品時。
當需要創建的各種產品差異不大時，可以使用 Builder 生成器模式。

