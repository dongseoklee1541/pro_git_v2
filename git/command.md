## commit
* git commit <option>
 * git commit -am "commit log" : -am은 커밋메시지와 add를 함께 해준다.
 * git commit --ammand : commit log 수정 

## log
### option
* -p : commit 간의 차이점을 보여줌
* --all : 모든 brach들도 함께 나옴
  * --all --graph --oneline : 브랜치를 시각적으로 보여주고(graph) 장황하지 않게 표기(oneline)

## Branch
* git branch : 현재 브랜치 이름

* git branch <name> : <name>의 이름을 가진 브랜치 생성
  * git branch google : google 브랜치 생성
 
* git checkout <name> : 해당하는 <name>의 브랜치로 변경 후 그 상태로 간다.
 
## Merge
master 상태일때 Merge해야 한다.(checkout master)

* git merge <branch-name> : Merge가 되고, 이때 어떤 이유로 merge하는지에 대해 작성해주면 된다.
 * git reset --hard <code> : merge를 되돌리고 싶다면 reset --hard 를 실행하자.
