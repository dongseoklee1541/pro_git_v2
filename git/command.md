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
master 상태일때 Merge해야 한다.(checkout master) 파일의 이름이 다르면 복사되어 병합되고, 같은 파일 이름이더라도 다른 부분이 수정된다면 merge된다.

* git merge <branch-name> : Merge가 되고, 이때 어떤 이유로 merge하는지에 대해 작성해주면 된다.
  * git reset --hard [code] : merge를 되돌리고 싶다면 reset --hard 를 실행하자.

### conflict
만약 merge를 할때, 같은 파일의 같은 라인이 동시에 변경이 되있다면 git은 merge할수 없는 상황이라고 알려준다. 이때 사용자가 직접 수정한 뒤
merge를 해줘야 한다..

## git remote push & clone & pull

### git push
local repo에서 원격 저장소(remote repo)로 보내기 위해선 절차가 필요하다.

1. local repo에서 원격 저장소를 지정한다.
 * git remote add origin(원격 저장소 이름, 자유롭게 해도 좋지만 원칙적으로 origin 사용) <원격저장소 주소> : 원격 저장소의 주소를 origin 이라는 이름으로 별명을 지어서 설정한다.
  * git remote : 위에서 orgin을 설정했다면, 원격 저장소의 주소를 알려준다.
  
2. 지정된 원격 저장소에 push를 하면 local repo의 있는 자료들이 업로드 된다.
 * git push : 원격 저장소에 파일 업로드
 * git push --set-upstream origin master : 처음 push를 한다면 이렇게 하자. 
 


