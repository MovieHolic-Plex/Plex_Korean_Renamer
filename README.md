PLEX Renamer and DB for KOREAN
==================


요구사항
--------

       pip install beautifulsoup4




개발배경
-------------
최근들어 토렌트 사이트에서 영어식 이름들과 여타의 plex 인식이 잘 되지 않는 파일들이 많아졌고,
누군가가 대신해서 Plex에 인식시킬 파일들의 이름을 관리해주는 건 어떤가 싶어서 만들어봤습니다.

아무래도 github는 처음이다 보니까 사용법을 잘 모릅니다만,
collarborator라는 게 협업자로서 파일의 수정권한을 갖고 있다는 것은 알겠습니다.

따라서 협업자 요청이 들어오면 협업자로서 등록할테니 names 파일을 규칙에 맞게 수정하시면 됩니다.


수정법은 간단합니다.
names을 열어보시면 이름들이 엔터로 구분되어 쭉 나열되어 있습니다.
예를 들면,

       One Piece ==>== 원피스

는 파일 이름에 [One Piece] 가 들어있으면 [원피스] 로 바꾸라는 의미입니다.
그 후, Renamer.py 를 작동시키시면 파일이름이 아래와 같이 변합니다.

       One Piece S01E02.HEVC.1080p-Outlow
에서 아래처럼 바뀝니다.

       원피스 S01E02.HEVC.1080p-Outlow

간단합니다. 이해가 안 되거나 필요한 기능이 있다면 언제든지 요청해주세요.
전공이 컴퓨터쪽은 아니지만 최대한 노력해보겠습니다.
추후 정규식같은 특수한 경우의 문자인식을 추가할 생각이 있습니다.


#### 규칙 ::
__1. ==>== 로 구분된 Names 파일의 한 행은 왼쪽 이름을 오른쪽 이름으로 변경(replace)한다.__

__2. ==>== 가 없는 행은 무시된다.__
