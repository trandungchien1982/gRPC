
# gRPC
Các ví dụ liên quan đến gRPC/ Demo thực tế từ cơ bản đến nâng cao<br/>
Mỗi nhánh trong Repo sẽ là 1 ví dụ/ giải pháp/ project mẫu liên quan đến gRPC

# Môi trường phát triển
- Sử dụng Protobuf (Protocol Buffer)
- Ngôn ngữ Java/Python

# Build Tools sử dụng
- Maven + Gradle
- Intelij IDEA

# Folder liên quan trên Windows
```
D:\Projects\gRPC
```

==============================================================

# Ví dụ [01.HelloWorld]
==============================================================

**Tham khảo:**<br/>
- https://200lab.io/blog/grpc-la-gi/
- https://co-well.vn/nhat-ky-cong-nghe/gioi-thieu-ve-grpc-cuc-huu-ich-cho-dev/
- https://blog.shiftasia.com/introduction-grpc-and-implement-with-spring-boot/
- https://github.com/lequanghuygialai/spring-grpc
- https://piotrminkowski.com/2023/08/29/introduction-to-grpc-with-spring-boot/
- https://www.baeldung.com/grpc-introduction

**Tạo ví dụ cơ bản để giao tiếp giữa 2 services sử dụng gRPC**
- `HelloRequest`, `HelloResponse` định nghĩa bằng Protobuf 
- Tạo Server/Client và gửi đi message `HelloRequest`, `HelloResponse` qua lại
- Mã nguồn tham khảo: https://github.com/lequanghuygialai/spring-grpc
- Sử dung IntelliJ IDEA plugin dành cho Protocol Buffer
- Project chính : `spring-grpc-master`, bao gồm 2 module con :
  - server-side
  - client-side
  - Code xài chung được tự động generate nằm trong folder `/gRPC/src/generated`: Profobuf/gRPC classes

**Workflow chi tiết**
- Define .proto file <br/>
  HelloService.proto
- Generate server and client code: <br/>
  `/gRPC/src/generated`
- Create server application, implement the generated service and spawn the gRPC server, make request with BloomRPC.
  https://github.com/bloomrpc/bloomrpc
- Create client application, make RPC call using generated stubs.
