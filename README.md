# VimStudy

vim 공식 튜토리얼 vimtutor 요약 모음 


### Lesson 1 요약

  1. 커서를 움직일 때에는 화살표 키나 hjkl 키를 이용합니다.
         h (왼쪽)       j (아래)       k (위)       l (오른쪽)

  2. 쉘 프롬프트에서 빔을 시작하려면 vim FILENAME <ENTER>

  3. 수정한 내용을 무시한 채로 빔에서 빠져나가려면   <ESC>   :q!   <ENTER>
                     저장한 후 빔에서 빠져나가려면   <ESC>   :wq   <ENTER>

  4. 명령 모드에서 커서가 위치한 곳의 글자를 지우려면   x  를 입력합니다.

  5. 명령 모드에서 커서가 위치한 곳에 텍스트를 삽입하려면
         i   를 누른 후 텍스트를 입력하고  <ESC> 를 누릅니다.

참고: <ESC>는 명령 모드로 돌아가는 데 쓰며, 원치 않는 명령이나 완전히 입력되지
      않은 명령을 취소하는 데에도 씁니다.

그럼 Lesson 2를 시작합시다.

### Lesson 2 요약 

  <br> 1. 커서가 위치한 곳부터 단어의 끝까지 지우려면:    dw
  <br> 2. 커서가 위치한 곳부터 줄 끝까지 지우려면:    d$
  <br> 3. 줄 전체를 지우려면:    dd
  <br> 4. 명령 모드에서 내리는 명령의 형식은 다음과 같습니다:

      [횟수]   명령   대상    또는    명령   [횟수]   대상 
      여기서:
       횟수 - 그 명령을 몇 번 반복할 것인가
       명령 - 어떤 명령을 내릴 것인가 ( 예를 들어, 삭제인 경우는 d )
       대상 - 명령이 동작할 대상, 예를 들어 w (단어), $ (줄의 끝) 등.

  <br> 5. 이전 행동을 취소하려면:                 u   (소문자 u)
  <br>    한 줄에서 수정한 것을 모두 취소하려면:   U   (대문자 U)
  <br>    취소한 것을 다시 실행하려면:            CTRL-R
     
 
 ### Lesson 3 요약

  1. 이미 지운 내용을 되돌리려면,  p  를 누르십시오. 
     이 명령은 커서 *다음에* 지워진 내용을 붙입니다(PUT). 
     ( 한 줄을 지운 경우에는 커서 다음 줄에 지워진 내용이 붙습니다.)

  2. 커서 아래의 글자를 치환하려면
     (REPLACE),  r  을 누른 후 원래 글자 대신 바꾸어 넣을 글자를 입력합니다.

  3. 변환 명령(CHANGE)은 커서에서 부터 지정한 대상의 끝까지 바꿀 수 있는
     명령입니다. 예를 들어, 커서 위치에서 단어의 끝까지 바꾸려면,  cw  를
     입력하면 되며,  c$  는 줄 끝까지 바꾸는 데 쓰입니다.

  4. 변환 명령의 형식은 다음과 같습니다:

         [횟수]   c   대상       또는       c   [횟수]   대상

계속해서 다음 Lesson 을 진행합시다.

### LESSON 4 요약

  1. CTRL-g  는 파일의 상태와 파일 내에서의 현재 위치를 표시합니다.
     SHIFT-G  는 파일의 끝으로 이동합니다. 줄번호를 입력한 후 SHIFT-G를
     입력하면, 그 줄로 이동합니다.

  2.  / 를 입력한 후 문구를 입력하면 그 문구를 아랫방향으로 찾습니다.
      ? 를 입력한 후 문구를 입력하면 윗방향으로 찾습니다.
     검색 후, n 을 입력하면 같은 방향으로 다음 문구를 찾으며,
     Shift-N 을 입력하면 반대 방향으로 찾습니다.

  3. 커서가 (,),[,],{,} 위에 있을 때에  % 를 입력하면 상응하는 짝을
     찾아갑니다.

  4. 어떤 줄에 처음 등장하는 old를 new로 바꾸려면          :s/old/new
     한 줄에 등장하는 모든 old를 new로 바꾸려면            :s/old/new/g
     두 줄 #,# 사이에서 치환을 하려면                      :#,#s/old/new/g
     파일 내의 모든 문구를 치환하려면                      :%s/old/new/g
     바꿀 때마다 확인을 거치려면 'c'를 붙여서              :%s/old/new/gc
     
     

### LESSON 5 요약

  1.  :!command  를 이용하여 외부 명령을 실행합니다.

      유용한 예:
         (MS-DOS)         (Unix)
          :!dir            :!ls            -  디렉토리의 목록을 보여준다.
          :!del FILENAME   :!rm FILENAME   -  FILENAME이라는 파일을 지운다.

  2.  :w FILENAME  하면 현재 빔에서 사용하는 파일을 FILENAME이라는 이름으로
      디스크에 저장합니다.

  3.  :#,#w FILENAME  하면 #부터 #까지의 줄을 FILENAME이라는 파일로 저장합니다.

  4.  :r FILENAME  은 디스크에서 FILENAME이라는 파일을 불러들여서 커서 위치
      뒤에 현재 파일을 집어넣습니다.
      
      
      
### LESSON 6 요약


  1.  o 를 입력하면 커서 *아래에* 한 줄이 열리며, 커서는 편집 모드로
     열린 줄 위에 위치하게 됩니다.
     대문자  O  를 입력하면 커서가 있는 줄의 *위로* 새 줄을 열게 됩니다.

  2.  a 를 입력하면 커서 *다음에* 글을 입력할 수 있습니다.
     대문자  A  를 입력하면 자동으로 그 줄의 끝에 글자를 추가하게 됩니다.

  3. 대문자  R  을 입력하면 <ESC> 를 눌러서 나가기 전까지 바꾸기 모드가 됩니다.

  4. ":set xxx" 를 하면 "xxx" 옵션이 설정됩니다.


### LESSON 7: 온라인 도움말 명령

                      ** 온라인 도움말 시스템 사용하기 **

  빔은 폭 넓은 온라인 도움말 시스템을 제공합니다.  도움말을 보려면,
  다음 세가지 중 하나를 시도해보십시오:
        - <HELP> 키를 누른다. (키가 있는 경우)
        - <F1> 키를 누른다. (키가 있는 경우)
        - :help <ENTER>   라고 입력한다.

  도움말 창을 닫으려면  :q <ENTER>  라고 입력하십시오.

  ":help" 라는 명령에 인자를 주면 어떤 주제에 관한 도움말을 찾을 수 있습니다.
  다음 명령을 내려 보십시오. ( <ENTER> 키를 누르는 것을 잊지 마십시오.)

        :help w
        :help c_<T
        :help insert-index
        :help user-manual
        
        
### LESSON 8: 시작 스크립트 만들기

                            ** 빔의 기능 켜기 **

  빔은 Vi 보다 훨씬 많은 기능을 가지고 있지만, 대부분은 기본적으로 작동하지
  않습니다. 더 많은 기능을 써보려면, "vimrc" 라는 파일을 만들어야 합니다.

  1. "vimrc" 파일을 수정합시다. 이 파일은 사용하는 시스템에 따라 다릅니다:
  1. Start editing the "vimrc" file, this depends on your system:
        :edit ~/.vimrc                  Unix의 경우
        :edit $VIM/_vimrc               MS-Windows의 경우

  2. 이제 "vimrc"의 예제를 읽어들입니다:

        :read $VIMRUNTIME/vimrc_example.vim

  3. 다음과 같이 하여 파일을 저장합니다:

        :write

  다음 번에 빔을 시작하면, 구문 강조(syntax highlighting)이 사용될 것입니다.
  모든 원하는 설정을 이 "vimrc" 파일에 넣어둘 수 있습니다.
