# [BUỔI 7] INTERFACE VÀ TRỪU TƯỢNG

---
## 1. Tính trừu tượng
---
- Tính trừu tượng là một tiến trình ẩn các cài đặt chi tiết và chỉ hiển thị tính năng tới người dùng. *Ví dụ: như tạo ra tính năng gửi tin nhắn, ta chỉ cần hiểu là người dùng viết tin rồi nhấn gửi đi. Còn quy trình xử lý tin nhắn gửi như thế nào thì ta chưa đề cập đến.*

-  Có 2 cách để đạt được sự trừu tượng:
    - Sử dụng lớp **Abstract**.
    - Sử dụng **Interface**.

## 2. Abstract class
---
- Khai báo **abstract class**:

``` Java
abstract  class  tên_lớp {
	các_thuộc_tính;
	các_phương_thức;
}
```
> Nếu mà một lớp có ít nhất một phương thức được định nghĩa là Trừu tượng, thì lớp đó phải khai báo Trừu tượng.
 
 - Khai báo **phương thức trừu tượng**:
 ```Java
 [khả_năng_truy_cập]  abstract  kiểu_trả_về  tên_phương_thức  ([ các_tham_số_truyền_vào"]);
 ```
 > Ví dụ: public abstract void print();

Một phương thức abstract không có thân phương thức, kết thúc bằng dấu `;`.

```Java
import java.util.Scanner;
abstract class Animal{
    abstract void say();
}
class Dog extends Animal{
    void say() {
        System.out.println("gau...gau...");
    }

    public static void main(String args[]) {
        Animal dog = new Dog();
        dog.say();
    }
}
```

> 
```Java
gau...gau...
```
 ## 3. Interface 
 ---
 - Một Interface không phải 1 lớp, nó là một tập hợp **các phương thức abstract**, có modifier là: **public abstract**.
- Interface luôn luôn có modifier là: **public interface**, cho dù bạn có khai báo rõ hay không.
- Interface **không có hàm** khởi tạo (constructor).
- Một interface không thể kế thừa từ lớp, nó được triển khai bởi một lớp.
- Cài đặt Interface, dùng từ khóa `implements`.
- So sánh giữa *Abstract class* và *Interface*:
---
| **Abstract Class**| **Interface** |
| ----------------- | ------------- |
| Khai báo bằng từ khóa Abstract | Khai báo bằng từ khóa Interface |
| Có phương thức abstract và non-abstract | Chỉ có phương thức abstract |
| Không hỗ trợ đa kế thừa | Hỗ trợ đa kế thừa |
| Ngoài biến static, final còn có các biến non-static, non-final | Chỉ có các biến static, final |


- Một lớp có thể triển khai 1 hoặc nhiều Interface.
- Một Interface có thể `extends` 1 Interface khác nhưng không `implements` 1 interface khác do interface chỉ chứa các phương thức mà không có các cài đặt. Một lớp chỉ `extends` được từ 1 lớp khác, nhưng `implements` được nhiều interface.














