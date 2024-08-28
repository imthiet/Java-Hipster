
# Index of JHipster

### 1.Tổng Quan Về JHipster



- [JHipster](#jhipster)
- [Technology stack của JHipster](#technology-stack)

### 2.Cài Đặt Môi Trường
- [2.1 Cài Đặt JHipster](#21-jhipster-installation)
- [2.2 Cấu Hình Proxy](#22-configuring-proxy)
- [2.3 Cấu Hình IDE](#23-configuring-ide)
- [2.4 Docker Compose](#24-docker-compose)
- [2.5 Shell Plugin](#22-configuring-proxy)





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



# 2. Cài Đặt Môi Trường
### 2.1 JHipster Installation
Có tới 4 cách để làm việc với JHipster.

**JHipster Online:**

 Cho phép tạo ra 1 ứng dụng JHipster mà không cần cài đặt JHipster. Được khuyến nghị cho người dùng mới hoặc người muốn có cái nhìn tổng quát về JHipster. Sau khi thiết lập cấu hình, có thể tải xuống ứng dụng dưới dạng file zip tương tự như spring initializr. Tuy nhiên phương thức này có những hạn chế về mặt tính năng cũng như trải nghiệm.

**Cài Đặt Trên Local với NPM:**

Yêu cầu:

 - Java 17 hoặc 21 LTS (Long Term Support)
 - Nodejs 64bit LTS version (không hỗ trợ phiên bản non-LTS)

Cài Đặt:
 - Câu lệnh cài đặt:
            
                 `npm install -g generator-jhipster`
 -  Nếu bạn muốn sử dụng một module hoặc một blueprint (chẳng hạn từ JHipster Marketplace), hãy cài đặt Yeoman:
            
                         `npm install -g yo`

Tùy chọn cài đặt khác:
    
- Java Build Tool: Nếu bạn sử dụng Maven hoặc Gradle, bạn hầu như không cần cài đặt bất cứ thứ gì, cũng như JHipster sẽ tự động cài đặt Maven/Gradle Wrapper cho bạn. Nếu không muốn sử dụng những Wrapper đó, truy cập trang web chính thức Maven hoặc Gradle để cài đặt theo ý mình.
- Cài đặt Git từ git-scm.com. Nên sử dụng công cụ SourceTree nếu bạn mới làm việc với git. Khi đó JHipster sẽ cố gắng commit dự án của bạn tới git. Ngoài ra *JHipster upgrade sub-generator* cũng yêu cầu Git được cài đặt.


**Cài Đặt Với Docker (Khuyến nghị cho chuyên gia):**

**Lưu ý**: Docker image này dùng để chạy JHipster generator bên trong một container. Nó hoàn toàn khác với các cấu hình Docker và Docker Compose mà JHipster sẽ tạo ra, có mục đích là chạy ứng dụng bạn đã tạo bên trong một container.

Thông Tin Chung:

- JHipster có một Dockerfile đặc biệt, nó cung cấp một Docker image.
- Nó làm cho một Docker "Automated Bulid" khả dụng trên:  https://hub.docker.com/r/jhipster/jhipster/
- Image này sẽ cho phép bạn chạy JHipster bên trong Docker.

Điều Kiện Tiên Quyết:


- (Được khuyến nghị) Docker Destop: cách dễ nhất để tạo, chạy, và kiểm tra 1 ứng dụng được docker hóa. Nó cung cấp giao diện người dùng cho các container/images/vokumes. Docker developer, Kubernetes và nhiều hơn nữa.

- Docker Engine: Ứng dụng client-server với giao diện dòng lệnh 

*Lưu Ý*: Dựa trên hệ điều hành của bạn, DOCKER_HOST sẽ khác nhau.

Sử Dụng Trên Linux/Mac Windows (với Docker)

- Pull the IMAGE
- Kéo JHipster Docker image mới nhất:
            
      `docker image pull jhipster/jhipster:master`
- Tất cả các Tag ở đây: https://hub.docker.com/r/jhipster/jhipster/tags/

*Cảnh báo*: Nếu bạn đang sử dụng Docker Machine trên Mac hoặc Windows, Docker daemon của bạn chỉ có quyền truy cập hạn chế vào hệ thống tệp của OS X hoặc Windows. Docker Machine cố gắng tự động chia sẻ thư mục `/Users` (trên OS X) hoặc `C:\Users\<username>` (trên Windows). Vì vậy, bạn phải tạo thư mục dự án trong những thư mục này để tránh gặp sự cố khi gắn kết volume.

- Tạo thư mục "jhipster" trong đường dẫn nhà của bạn:

                  `mkdir ~/jhipster`

- Khởi chạy Docker Image : 

    `docker container run --name jhipster -v ~/jhipster:/home/jhipster/app -v ~/.m2:/home/jhipster/.m2 -p 8080:8080 -p 9000:9000 -p 3001:3001 -d -t jhipster/jhipster`
- Kiểm tra nếu container đang chạy, sử dụng lệnh `docker container ps`
- Lệnh dừng Docker: `docker container stop jhipter`
- Khởi chạy lại: `docker container start jhipster`
- Trong trường hợp cập nhật Docker Imamge, nên xóa những container đang có và chạy lại từ đầu:

    `1.docker container stop jhipster

    2.docker container rm jhipster

    3.docker image pull jhipster/jhipster

    4.docker container run --name jhipster -v ~/jhipster:/home/   jhipster/app -v ~/.m2:/home/jhipster/.m2 -p 8080:8080 -p 9000:9000 -p 3001:3001 -d -t jhipster/jhipster`

TRUY CẬP CONTAINER

Câu lệnh:

           `docker container exec -it <container_name> bash`

Với jhipster:

            `docker container exec -it jhipster bash`

Bạn sẽ đăng nhập như 'jhipster'

Trong trường hợp bạn muốn đăng nhập với "root":

    `docker container exec -it --user root jhipster bash

`
ỨNG DỤNG ĐẦU TIÊN
- Có thể truy cập tới /home/jhipster/app ở trong container và bắt đầu xây dựng ứng dụng bên trong Docker:

    `cd /home/jhipster/app`
- Khi ứng dụng đã được khởi tạo, bạn có thể sử dụng tất cả các lệnh của gulp/bower/maven : `./mvnw`

**HOÀN THÀNH KHỞI CHẠY ỨNG DỤNG JHIPSTER BÊN TRONG DOCKER**

- Truy cập ứng dụng đang chạy: `http://DOCKER_HOST:8080`.
- Truy cập vào tất cả các file được tạo ra trong thư mục shared.
**Cảnh báo**: Mặc định, Docker không được cài đặt trong image `jhipster/jhipster`. Do đó, bạn sẽ không thể:

- Sử dụng các file `docker-compose`.
- Xây dựng một image Docker với Docker daemon (Maven goal: `jib:dockerBuild` hoặc Gradle task: `jibDockerBuild`).

Tuy nhiên, bạn có thể sử dụng chế độ không cần daemon của Jib, chế độ này có thể xây dựng một image Docker và đẩy nó lên một registry mà không cần truy cập vào Docker daemon (Maven goal: `jib:build` hoặc Gradle task: `jibBuild`). Nhưng bạn sẽ cần thiết lập thông tin đăng nhập vào Docker registry như một yêu cầu trước khi xây dựng ứng dụng. Xem tài liệu cấu hình của plugin Jib để biết thêm chi tiết.

### 2.2 Configuring Proxy


#### Cấu hình Proxy Doanh Nghiệp

Khi JHipster được sử dụng trong một công ty, bạn có thể cần cấu hình tất cả các công cụ để vượt qua proxy doanh nghiệp.

Bạn có thể thử cấu hình các biến môi trường `HTTP_PROXY` và `HTTPS_PROXY` hoặc sử dụng công cụ như Cntlm.

Tuy nhiên, điều này có thể chưa đủ, vì vậy bạn sẽ cần phải cấu hình riêng biệt cho tất cả các công cụ được sử dụng cùng với JHipster.

- Proxy được định hình bởi:

        username - password - host- port
- Dường dẫn : http://username:password@host:port. Nếu sử dụng Cntlm, config của bạn sẽ là: 127.0.0.1:3128


 
### 2.3 Configuring IDE

Một dự án JHipster có thể được phát triển mà không cần bất kì IDE nào. Bạn chỉ cần một trình chỉnh sửa đơn giản và command line. Trên thực tế, ta cần sử dụng một IDE hoặc một trình soạn thảo nâng cao hơn. Sau đây là một số cách cài đặt:

-Cấu hình Eclipse với Maven: https://www.jhipster.tech/configuring-ide-eclipse/

-Cấu hình Eclipse với Gradle: https://www.jhipster.tech/configuring-ide-eclipse-gradle/

-Cấu hình Intellij IDEA: https://www.jhipster.tech/configuring-ide-idea/

-Cấu hình VSCode:https://www.jhipster.tech/configuring-ide-visual-studio-code/

-Cấu hình Netbean:https://www.jhipster.tech/configuring-ide-netbeans/


### 2.4 Docker Compose

 - Kiểm tra xem docker đã cài đặt hay chưa:

                `docker --veriosn`
- Khởi chạy dự án với JHipster:
![Description](assert/generateApp.png)

Nếu sử dụng Cassandra chạy lệnh : 

`docker-compose -f src/main/docker/cassandra.yml up`


migrate thành công:

![Result](assert/migrate.png)

Run ứng dụng thành công, cổng 8080:

![Result](assert/image.png)

Giao diện trên localhost:8080:
ảnh local

### đã khởi chạy thành công! ###

