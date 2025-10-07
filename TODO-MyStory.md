TODO-MyStory.md


멤버활동 기록
- MongoDB member_activites 에서 데이터를 N page 만큼 들고온다.
- 들고온 MemberActivity 도큐먼트 타입 데이터를 MyStory 타입으로 변환한다.
- MyStory 타입의 하위타입은 MyCommentStory, MyPostStory, MyMemberStory 가 있다.
- MyCommentStory, MyPostStory, MyMemberStory 로 변환하는 기준은 ActivityType (POST_CREATE, POST_LIKE 등)을 기반으로 수행한다.
- 특정 하위 타입으로 생성해주는 메서드는 별도의 컴포넌트에 작성하며 resolver 라는 패키지 내에 StoryResolver 라는 클래스 내에 resolve() 라는 이름으로 만든다.
- converter 라는 이름을 사용하고 싶었지만 그러지 않은 이유는 MongoDB의 타입 Converter, JPA 의 Type Converter 와 혼용될 가능성이 너무 많아서다.
- 각 타입별로 댓글 정보가 필요할 수도 있고 어떤건 작성자 이름정보, 글 주소 등을 알아야할 수 있다.




