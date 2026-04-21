# Spring H2 Database And Flyway Template

---

## application.properties

```properties
spring.application.name=ProjectNameHere

spring.datasource.url=jdbc:h2:mem:testdb;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE
spring.datasource.driver-class-name=org.h2.Driver
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect

#JPA
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

#Flyway
spring.flyway.enabled=true
spring.flyway.locations=classpath:db/migrations
spring.flyway.baseline-on-migrate=true
```

---

## db/migrations/V1__create_table.sql

> ⚠️ Attention: Flyway requires **two underscores** between the version and the filename.

> ✅ `V1__create_table.sql`
> ❌ `V1_create_table.sql`

> 📊 Table example

```sql
CREATE TABLE tb_name (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    column_1 VARCHAR(255),
    column_2 VARCHAR(255),
    column_3 INT,
    column_4 TIMESTAMP
    -- add column here
);
```
