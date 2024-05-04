1. 배경색 지정과 프로필 아이콘, 상태 메시지 생성.
2. 생성된 아이콘을 예제와 같이 정렬하는데 실패함.
-----


- [ ] HTML 구조 설계
1.  div 태그를 사용해 아바타 아이콘을 모아주었습니다.
2. 사용자의 사진을 보여주는 아이콘을 img태그를 사용해 콘텐츠 이미지로 삽입했고, div태그로 접속상태가 online인지 offline인지 구분해주는 원을 삽입했습니다.
3. 3단 구조로 이루어진 avatars-status아이콘 8개를 만들었습니다.
4. Avatars-status에는 사용자의 접속상태, face에는 어느 사용자인지, icon에는 접속중인지 아닌지 aria-lable을 사용해 명시했습니다.

- [ ] CSS 스타일 적용

1. 아이콘 배경(wrap-avatars) - 첫 번째 사용된 class name wrap-avatars에 배경색으로 ivoy를 지정하고 width 값을 지정하여 화면 너비를 줄여도 아이콘이 밀려나지 않도록 했습니다. Min-height 값으로 최소 높이를 지정하여 요소가 늘어나거나 줄어들어도 컨텐츠 영역이 보장받도록 안정성을 높였습니다. Padding에 값을 주어 아이콘이 중앙에 위치한 것 처럼 보이도록 했습니다. Display를 flow-root로 지정해 자식요소를 인식시키도록 했습니다.

2. 상태 아이콘이 포함된 아바타 아이콘(avatars-status) - float에 left 값을 주어 왼쪽부터 띄워지도록 배치하고 padding에 10px를 주어 아이콘과 아이콘 간격을 20px로 맞추었습니다. position에 relative 값을 넣어 상태 아이콘의 위치기준을 잡아줬습니다.

3. 사용자 얼굴 아이콘(face) -크기를 width, height 각 64px를 지정해 맞추고 border-radius 100%를 주어 둥근 형태를 갖추었습니다. float에 left 값을 주어 왼쪽부터 띄워지도록 배치했습니다.

4. 상태 아이콘(icon) - 크기를 width, height 각 14px를 지정해 맞추고 border-radius 100%를 주어 둥근 형태를 갖추었습니다. position에 absolute, margin tpp과 left에 48px씩 주어 예제 이미지와 비슷한 위치로 조정했습니다.

5. 줄바꿈 시점(avatars-status) - nth-child(5), clear: left로 5번째 요소부터 줄바꿈 되도록 지정했습니다.

6. 상태 아이콘 접속, 비접속 여부 - 자식 선택 요소로 접속중인 사용자는 형광초록색, 비접속 사용자는 회색이 나타나도록 지정했습니다.

7. Flex 지원 환경에서는 남성 사용자와 여성사용자의 배치가 바뀌도록 flex-flow를 행방향 진행, 역순배열로 지정했습니다.