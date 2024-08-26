
# Index of JHipster

### 1.Tổng Quan Về JHipster



- [JHipster](#jhipster)
- [Technology stack của JHipster](#technology-stack)
- [Test](#test)





# 1.Tổng Quan Về JHipster
### JHipster
JHipster là một nền tảng phát triển giúp nhanh chóng tạo ra, phát triển, và triển khai các ứng dụng web hiện đại và kiến trúc microservice. Nền tảng này hỗ trợ nhiều công nghệ frontend như Angular, React, và Vue, và thậm chí còn hỗ trợ phát triển ứng dụng di động với Ionic và React Native. Ở phía backend, JHipster hỗ trợ Spring Boot (với Java hoặc Kotlin), Micronaut, Quarkus, Node.js, và .NET. Về triển khai, JHipster tuân theo các nguyên tắc cloud-native với Docker và Kubernetes. Nền tảng này cũng hỗ trợ triển khai trên các dịch vụ như AWS, Azure, Cloud Foundry, Google Cloud Platform, Heroku, và OpenShift.

### Technology Stack

**Phía Client:**


- **Ứng dụng Web đơn trang (Single Web Page Application):**
  - Angular, React hoặc Vue
  - Thiết kế Web đáp ứng (Responsive Web Design) với Twitter Bootstrap
  - HTML5 Boilerplate
  - Tương thích với các trình duyệt hiện đại (Chrome, Firefox, Microsoft Edge…)
  - Hỗ trợ đầy đủ quốc tế hóa (Internationalization)
  - Tùy chọn hỗ trợ Sass cho thiết kế CSS
  - Tùy chọn hỗ trợ WebSocket với Spring Websocket
  - Với quy trình phát triển mạnh mẽ:
    - Cài đặt các thư viện JavaScript mới với NPM
    - Xây dựng, tối ưu hóa và tải lại trang tự động với Webpack
    - Kiểm thử với Jest và Protractor
  - Và nếu một ứng dụng Web đơn trang không đủ cho nhu cầu của bạn?
    - Hỗ trợ cho công cụ template Thymeleaf để tạo trang Web trên phía server

**Phía server:**

- **Một ứng dụng Spring hoàn chỉnh:**
  - Spring Boot để cấu hình ứng dụng
  - Cấu hình Maven hoặc Gradle để xây dựng, kiểm thử và chạy ứng dụng
  - Cấu hình "development" và "production" (cho cả Maven và Gradle)
  - Spring Security
  - Spring MVC REST + Jackson
  - Tùy chọn hỗ trợ WebSocket với Spring Websocket
  - Spring Data JPA + Bean Validation
  - Cập nhật cơ sở dữ liệu với Liquibase
  - Hỗ trợ Elasticsearch nếu bạn muốn có khả năng tìm kiếm trên cơ sở dữ liệu của mình
  - Hỗ trợ MongoDB và Couchbase nếu bạn muốn sử dụng cơ sở dữ liệu NoSQL hướng tài liệu thay vì JPA
  - Hỗ trợ Cassandra nếu bạn muốn sử dụng cơ sở dữ liệu NoSQL hướng cột thay vì JPA
  - Hỗ trợ Kafka và Pulsar nếu bạn muốn sử dụng hệ thống tin nhắn publish-subscribe

Hệ công nghệ cho microservices:

- **Microservices là tùy chọn và được hỗ trợ đầy đủ:**
  - Định tuyến HTTP sử dụng Spring Cloud Gateway
  - Khám phá dịch vụ sử dụng HashiCorp Consul hoặc Netflix Eureka

- **Sẵn sàng để triển khai vào sản xuất:**
  - Giám sát với Metrics và ELK Stack
  - Lưu trữ tạm thời (Caching) với ehcache (bộ nhớ đệm cục bộ), Caffeine (bộ nhớ đệm cục bộ), Hazelcast, Infinispan, Memcached hoặc Redis
  - Tối ưu hóa tài nguyên tĩnh (bộ lọc gzip, HTTP cache headers)
  - Quản lý log với Logback, có thể cấu hình trong thời gian chạy
  - Kết nối pool với HikariCP để có hiệu suất tối ưu
  - Tạo file WAR tiêu chuẩn hoặc file JAR thực thi
  - Hỗ trợ đầy đủ Docker và Docker Compose
  - Hỗ trợ cho tất cả các nhà dịch vụ đám mây chính: AWS, Cloud Foundry, GCP, Heroku, Kubernetes, OpenShift, Azure, Docker…



### Test
