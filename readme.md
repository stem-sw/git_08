## 준비물

- Git이 설치된 컴퓨터
- GitHub 계정
- 미리 복제(`clone`)한 실습 저장소
- 저장소 안의 `profile.md` 파일

> 아래 명령어는 **실습 저장소 폴더의 터미널**에서 실행합니다.  
> 명령어의 `본인GitHub아이디`는 실제 본인의 GitHub 아이디로 바꾸세요.  
> 예: `feature/octocat`

## 제출 결과물

다음 세 가지를 제출합니다.

1. 병합이 완료된 Pull Request 주소(URL)
2. Pull Request의 **Files changed** 화면 캡처
3. 마지막 `git log --oneline -5` 실행 결과 캡처

## 단계별 실습

### 1단계. `main` 브랜치 최신 상태 받기

```bash
git switch main
git pull origin main
```

### 2단계. 개인 작업 브랜치 만들기

```bash
git switch -c feature/본인GitHub아이디
```

브랜치가 바뀌었는지 확인합니다.

```bash
git branch --show-current
```

### 3단계. `profile.md` 수정하기

`profile.md`를 열고 자신의 GitHub 아이디와 한 줄 소개를 작성합니다.

```md
# 나의 프로필

- GitHub 아이디: 본인GitHub아이디
- 한 줄 소개: GitHub Pull Request를 실습하고 있습니다.
```

파일을 저장한 뒤 변경 내용을 확인합니다.

```bash
git status
```

### 4단계. 수정 내용 커밋하기

```bash
git add profile.md
git commit -m "docs: add my profile"
```

### 5단계. 개인 브랜치 GitHub에 올리기

```bash
git push -u origin feature/본인GitHub아이디
```

### 6단계. Pull Request 만들기

1. GitHub에서 실습 저장소 페이지를 엽니다.
2. **Compare & pull request** 버튼을 클릭합니다.
3. 브랜치를 다음과 같이 선택합니다.
   - **base:** `main`
   - **compare:** `feature/본인GitHub아이디`
4. 제목에 `Add 본인GitHub아이디 profile`을 입력합니다.
5. **Create pull request**를 클릭합니다.

### 7단계. 변경 내용 확인하고 병합하기

1. Pull Request의 **Files changed** 탭을 클릭합니다.
2. `profile.md`만 원하는 내용으로 변경되었는지 확인합니다.
3. 제출용 화면을 캡처합니다.
4. Pull Request의 첫 화면으로 돌아갑니다.
5. **Merge pull request**를 클릭한 뒤 **Confirm merge**를 클릭합니다.

화면에 **Pull request successfully merged and closed**가 표시되면 병합이 완료된 것입니다.

### 8단계. 로컬 `main`에서 최종 결과 확인하기

터미널로 돌아와 다음 명령어를 실행합니다.

```bash
git switch main
git pull origin main
git log --oneline -5
```

최근 커밋 목록에 자신의 프로필 수정 또는 Pull Request 병합 기록이 보이는지 확인하고, 제출용 화면을 캡처합니다.

## 최종 체크리스트

- [ ] `main`에서 `git pull origin main`을 실행했다.
- [ ] `feature/본인GitHub아이디` 브랜치를 만들었다.
- [ ] `profile.md`에 본인 정보를 작성했다.
- [ ] 수정 내용을 `add`, `commit`, `push`했다.
- [ ] `base: main`, `compare: feature/본인GitHub아이디`로 Pull Request를 만들었다.
- [ ] **Files changed**에서 변경 내용을 확인했다.
- [ ] **Merge pull request**로 병합했다.
- [ ] 로컬 `main`에서 다시 `git pull origin main`을 실행했다.
- [ ] `git log --oneline -5`로 최종 결과를 확인했다.
- [ ] Pull Request 주소와 캡처 2장을 준비했다.
