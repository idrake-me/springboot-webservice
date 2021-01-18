# 스프링 부트와 AWS로 혼자 구현하는 웹 서비스




## Chapter 3 

Entity의 PK
 - Long 타입의 Auto_increment 추천
 
@Setter
 - Entity Class는 Setter를 생성하지 않음
 - 생성자를 통해 최종값을 채운후에 DB에 저장
 - 해당 이벤트에 맞는 public 메소드를 호출하여 변경 
 - @Builder를 통해 제공되는 빌더 클래스를 사용
 
 Repository 위치 
  - Entity Class와 같은 위치에서 관리 
  - 나중에 분리할 경우에 이점이 존재
  
 Service에서의 비즈니스 로직 처리?
  - 처리하지 않고 트랜잭션, 도메인 간 순서 보장의 역활만
  - Domain에서 처리(즉, 객체에서 처리)
  
 Bean 주입 방법
  - @Autowired
  - setter
  - ***생성자*** @RequiredArgsConstructor : final이 선언된 모든 필드를 인자값으로 하는 생성자
  
 Entity Class를 DTO Class로 사용 X
 
