FROM maven:3.8.4-openjdk-8
WORKDIR /opt/server
COPY pom.xml .
COPY src /opt/server/src
RUN mvn clean package
RUN mv /opt/server/target/shipping-1.0.jar /opt/server/shipping.jar
ENV CART_ENDPOINT="cart:8080" \
    DB_HOST="mysql" \
    SPRING_DATASOURCE_URL="jdbc:mysql://mysql:3306/cities?useSSL=false&allowPublicKeyRetrieval=true&useUnicode=true&characterEncoding=UTF-8"
CMD ["java", "-Dserver.port=8080", "-Dserver.address=0.0.0.0", "-jar", "shipping.jar"]


# FROM maven
# WORKDIR /opt/server
# COPY pom.xml .
# COPY src /opt/server/src
# RUN mvn clean package
# RUN mv /opt/server/target/shipping-1.0.jar /opt/server/shipping.jar
# ENV CART_ENDPOINT="cart:8080" \
#     DB_HOST="mysql"
# CMD ["java","-jar","shipping.jar"]