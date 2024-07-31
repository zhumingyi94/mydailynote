# Object orientation 

## MAIN CONTENT

**OBJECTIVE:** Nói về abstraction, encapsulation, modularity và hierachy. Mô tả mối quan hệ giữa các class, tính đa hình và tính tổng quát 

**OBJECTS:** Thường mô tả một thực thể (entity), có thể thuộc các dạng sau
![[Pasted image 20240716013306.png | center]]
=> *More formal definition:* Object là một thực thể với boundary được định nghĩa rõ ràng và có đầy đủ state và behavior trong đó:
- State được mô tả bởi các attribute và relationship 
- Behavior được mô tả bởi cấc toán tử, methods, ...
VD:
STATE của objects
![[Pasted image 20240716013722.png | center]]
BEHAVIOR của objects
![[Pasted image 20240716013730.png |center]]

Mỗi objects là riêng biệt kể cả state có trùng nhau hoàn toàn:
![[Pasted image 20240716013839.png | center]]

4 tính chất chính của OO Design:
- Abstraction: Tập hợp những đặc điểm cơ bản của thực thể mà phân biệt nó với mọi loại thực thể khác 
- Encapsulation 
- Modularity: Break những thành phần phức tạp thành những thành phần cơ bản dễ hiểu, VD:
![[Pasted image 20240716014149.png | center]]
- Hierarchy:
![[Pasted image 20240716014246.png | center]]

**CLASS:** Blueprint của các objects giống nhau 

#### POLYMORPHISM AND GENERALIZATION

- **Polymorphism:** The ability to hide many different implementations behind a single interface
- **Generalization**: A relationship among classes where one class shares the structure and/or behavior of one or more classes.