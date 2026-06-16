# 愛你 (아이니) 단어장

王心凌 「愛你」 가사로 만든 중국어 단어 암기 웹앱.
단어 → 어절 → 문장 3단계, 음성 듣기(TTS), 카드/리스트 보기, 진행률 자동 저장.

## 폴더 구성

```
aini-deck/
├── index.html                  ← 단어장 본체 (이 파일 하나가 전부)
├── README.md
└── .github/workflows/deploy.yml ← GitHub Pages 자동배포 설정
```

## GitHub에 올리고 자동배포 켜는 법

### 1. 저장소 만들기
GitHub에서 새 저장소(repository) 생성. 이름은 자유 (예: `aini-deck`).

### 2. 파일 올리기
이 폴더 안의 파일들을 그대로 push.

```bash
cd aini-deck
git init
git add .
git commit -m "단어장 첫 배포"
git branch -M main
git remote add origin https://github.com/<내아이디>/<저장소이름>.git
git push -u origin main
```

웹에서 드래그&드롭으로 올려도 되지만, `.github/workflows/deploy.yml`은 폴더 구조가 유지돼야 하므로 git push를 권장.

### 3. Pages 활성화 (한 번만)
저장소 → **Settings → Pages → Build and deployment → Source**를 **GitHub Actions**로 선택.

### 4. 끝
push할 때마다 Actions가 자동으로 배포. 주소는
`https://<내아이디>.github.io/<저장소이름>/`

배포 진행 상황은 저장소의 **Actions** 탭에서 볼 수 있어요.

## 앞으로 수정할 때

`index.html`만 고쳐서 다시 push하면 1~2분 뒤 사이트가 자동 갱신됩니다.

```bash
git add index.html
git commit -m "단어 수정"
git push
```
