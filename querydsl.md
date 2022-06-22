# Query Dsl Cheat Sheet







## Gradle 설정

- enable annotation processor 설정

```groovy
dependencies {
    //...
        implementation "com.querydsl:querydsl-core"
    implementation "com.querydsl:querydsl-jpa"

    annotationProcessor("com.querydsl:querydsl-apt:${dependencyManagement.importedProperties['querydsl.version']}:jpa") // querydsl JPAAnnotationProcessor 사용 지정
    annotationProcessor("jakarta.persistence:jakarta.persistence-api") // java.lang.NoClassDefFoundError(javax.annotation.Entity) 발생 대응
    annotationProcessor("jakarta.annotation:jakarta.annotation-api") // java.lang.NoClassDefFoundError (javax.annotation.Generated) 발생 대응
    //...
    
}

```

> ​	http://honeymon.io/tech/2020/07/09/gradle-annotation-processor-with-querydsl.html

