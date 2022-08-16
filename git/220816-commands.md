Today

1. git을 사용하기 위한 CLI Shell command
2. git 맛보기(add, commit, push flow 확인)


1. CLI ? Shell?
  - Command Line Interface 
  - 터미널을 통해 사용자와 컴퓨터가 상효작용하는 방식.
  - Shell은 커널과 사용자를 연결해주는 역할. 

  - Shell Command
**~** (tild) : 지금 로그인한 사용자가 자유롭게 사용할 수 있는 최상위 위치
**ls** (list segment) : 현 위치에서 접근할 수 있는 하위 directory 들을 보여줌
**cd** (change directory) : 내(사용자) 위치 변경
**..** : 상위directory
→ cd .. : 상위directory로 옮겨간다.

**-** : flag 활성화 / flag는 on, off의 역할
**-a** (all file) : 숨김파일까지 보여줘
-l (line by line) : 자세히
**ls -al :** 하위directory 숨김파일까지 line by line으로 자세히 보여줘.
**mkdir** (make directory)
(+ unix like os 는 파일(directory)tou이름 앞에 . 붙이면 숨김파일)
**touch** : 파일생성 / 텍스트기반 파일들은 만들수 있으나, 특정한 어플리케이션을 통해서 만들어야하는 .db, .hwp, .xlsx 종류의 파일들은 touch를 통해서 생성할 수는 없다.
**mv** : move
→ mv ../ Afile ./ : ../ (상위폴더의) Afile을 ./ (현재위치로)
mv Afile Bfile : Afile 파일의 이름을 Bfile 로 바꾼다.
( 현재위치라는것을 생략하지 않는다면 mv ./old.py ./new.py 겠지)

**cp** (copy)
cp Afile ./Afile-copy → ./(현재위치로)Afile-copy 복사할때는 이름 다르게 써야지 그냥 현재위치까지만 적으면 덮어쓰기가 되어버림.
**rm** (remove)
(remove는 논리적인 삭제.접근할수있는 방법을 차단하는. hdd상에는 남아있음. / delete는 물리적인 삭제)

**rm -r directory명** :(recursive) directory 안에 있는 파일들을 다 지우고 해당 directory까지 지워라


2. git 맛보기
  - version control system
  - source code management

2-1. git process flow
  (github에서 remote repository 먼저 생성 하고 내 작업공간에 clone 만들어서 작업하는 방식으로)
  $ git clone 복사한 remote repo 주소 (local repo 생긴 셈)

  내가 작업하는 working directory 에서 할일을 한다(파일을 만들거나 수정하거나)
  -> git add 작업물  (staging area에 올려둬서 commit 할 수 있는 상태가 됨)
  -> git commit   (local repo에 commit 됨. commit 할 때에는 conventional commit 에 맞춰 제목,내용적기)
  -> git push   (github remote repo에다가)

  중간중간 git status로 어느단계인지, 상태 확인해줄것

