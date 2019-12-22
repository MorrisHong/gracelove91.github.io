---
title: "[JUnit5] 기본어노테이션"
last_modified_at: 2019-12-23
categories:
  - TEST
tags:
  - Post Formats
  - readability
  - standard
---
-   스프링부트 2.2부터 JUnit5가 기본적으로 의존성에 추가된다.
-   클래스와 테스트메서드에 더이상 public 접근제한자 설정 안해줘도 된다. package-private으로 설정하면 된다.

### @Test

-   JUnit4의 @Test와 같은 애너테이션이라고 이해하면 된다.

### @BeforeAll

-   모든 테스트메서드가 실행하기 전 딱 한 번만 호출한다.
-   static void 여야한다

### @AfterAll

-   모든 테스트메서드가 실행한 후 딱 한 번만 호출한다.
-   static void 여야한다

### @BeforeEach

-   개별 테스트 메서드가 실행되기 전 호출한다.

### @AfterEach

-   개별 테스트 메서드가 실행한 후 호출한다

### @Disabled

-   테스트 메서드 위에 붙이면 그 테스트는 Ignored 된다.

### 기본적인 테스트 코드

```
class BasicTest {
    @Test
    void test1() {
        System.out.println("test1");
    }

    @Test
    void test2() {
        System.out.println("test2");
    }

    @BeforeAll
    static void beforeAll() {
        System.out.println("beforeAll");
    }


    @AfterAll
    static void afterAll() {
        System.out.println("afterAll");
    }

    @BeforeEach
    void beforeEach() {
        System.out.println("beforeEach");
    }

    @AfterEach
    void afterEach() {
        System.out.println("afterEach");
    }
}
```

-   실행 순서
    
    beforeAll() => beforeEach() => test1() => afterEach() => beforeEach() => test2() => afterEach() => afterAll()
    

### JUnit4와 JUnit5의 대응 애너테이션

<table style="border-collapse: collapse; width: 100%;" border="1" data-ke-style="style3"><tbody><tr><td style="width: 50%; text-align: center;"><b>JUnit4</b></td><td style="width: 50%; text-align: center;"><b>JUnit5</b></td></tr><tr><td style="width: 50%;">@Test</td><td style="width: 50%;">@Test</td></tr><tr><td style="width: 50%;">@BeforeClass</td><td style="width: 50%;">@BeforeAll</td></tr><tr><td style="width: 50%;">@AfterClass</td><td style="width: 50%;">@AfterAll</td></tr><tr><td style="width: 50%;">@Before</td><td style="width: 50%;"><span style="color: #333333;">@BeforeEach</span></td></tr><tr><td style="width: 50%;">@After</td><td style="width: 50%;">@AfterEach</td></tr><tr><td style="width: 50%;">@Ignored</td><td style="width: 50%;">@Disabled</td></tr></tbody></table>