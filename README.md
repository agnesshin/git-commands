## Git Command

1. git add filename (한건씩 추가 한다, 최대 작은 건수도 staging된다)
2. git status (첫번쨰, 무족건 확인 후 git add 진행)
3. git status (add된 내용 잘 올라갔는지 확인)
4. git commit ( i 눌러서 insert mode > 내용 최대한 구체적으로 적어준다 > ESC > :wq! + enter)
5. git log (현재 up to date 되어있는지 다시 한번 확인, :wq + enter)
6. git rebase -i feature/ 현재 작업 브랜치 (작업하는 브랜치 현재 파일 올리준다)
7. git push origin feature/현재 작업 브랜치
8. git checkout feature/my-page (브랜치 이동)
9. git pull origin feature/my-page (이동 브랜치에서 pull 땡겨오기)
10. git push upstream (source tree에서 commit, rebase 한 내용 맨위로 올라가기 보이다)
11. git push origin feature/icon-list -f ( ! [rejected] error: failed to push some refs to '해댕 repository')

=================

Reset vs. Revert 차이점-> Reset을 과거로 한단계로 돌아간단, 위에 히스토리ㄹ를 지워준다-> Revert 이떄의 변화를 거꾸루 수행할는 캡슐을 하나 넣음으로 쓴다.

명령어:**git revert** (이전 파일- 돌아간다, 협업 할떄 revert 사용함, revert 하면서 conflict 발생 될 경우, conflict 해결 우선으로 진행)

**git add/rm <path spec>** (참고: path spec은 커밋 넘버와 동일)

=================

추가로... 공통 작업하는 부분, push 후, rebase 받아서 up to date 까지되면 작업 진행 가능하다

1. git stash (브랜치 이동 전, 작업하는 브랜치 내용 저장해준다)
2. git checkout feature/mypage (브랜치 이동)
3. git rebase (Successfully rebased and updated refs/head/feature/my-page-적용 잘된 메세지)
4. git checkout feature/작업하는 브랜치 이동
5. git stash pop (할 경우, 이전 브랜치 이동 전, 개인 작업 파일 살려준다. 업데이트 부분 다시 작업 진행)

=================

> Source Control > Staging, unstaging

**Staging**

1. git status (작업 내용 확인)

2. git add . (필수 아님, Source control에서 staging 되는 현황 확인 후, 두개 이상 있을 경우, 하나 unstaging으로 하고 나서 ....)

3. git commit -m "Update text-gray-700"

4. 작업 진행
