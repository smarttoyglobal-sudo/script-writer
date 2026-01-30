# 📺 감동/휴먼 콘텐츠 대본 작성기 - 배포 가이드

## 🚀 배포 방법 (10분이면 끝)

### 1단계: GitHub에 코드 올리기

1. **GitHub 접속** → https://github.com
2. **새 저장소 만들기** → "New repository" 클릭
3. **저장소 이름**: `script-writer` (원하는 이름)
4. **Private 선택** (코드 비공개)
5. **파일 업로드**: `app.py`, `requirements.txt` 업로드

### 2단계: Streamlit Cloud 배포

1. **Streamlit Cloud 접속** → https://share.streamlit.io
2. **GitHub 계정 연결**
3. **"New app" 클릭**
4. **설정**:
   - Repository: `your-username/script-writer`
   - Branch: `main`
   - Main file path: `app.py`

### 3단계: API 키 설정 (⚠️ 중요!)

1. 앱 배포 화면에서 **"Advanced settings"** 클릭
2. **"Secrets"** 탭 선택
3. 아래 내용 입력:

```toml
ANTHROPIC_API_KEY = "sk-ant-api03-여기에-실제-API키-입력"
```

4. **"Save"** 클릭
5. **"Deploy"** 클릭

### 4단계: 완료!

배포 완료 후 이런 링크가 생성됩니다:
```
https://your-app-name.streamlit.app
```

이 링크를 다른 사람에게 공유하면 됩니다!

---

## 💰 비용 구조

| 항목 | 비용 | 부담 |
|------|------|------|
| Streamlit Cloud | **무료** | - |
| Anthropic API | **사용량만큼** | 주철님 계정 |

### API 비용 예시 (Claude Sonnet 기준)
- 대본 1개 작성: 약 $0.01~0.03 (약 15~40원)
- 하루 100개 작성해도: 약 $1~3 (약 1,500~4,000원)

---

## 🔒 보안

✅ **숨겨지는 것**:
- 시스템 프롬프트 (지침 전체)
- API 키

❌ **사용자가 볼 수 있는 것**:
- 입력창
- AI 응답 결과

---

## ❓ FAQ

**Q: PC 켜놔야 하나요?**
A: 아니요! Streamlit Cloud가 24시간 서버 역할을 합니다.

**Q: 사용자가 지침을 볼 수 있나요?**
A: 아니요. 시스템 프롬프트는 백엔드에서만 작동합니다.

**Q: 비용은 어떻게 나가나요?**
A: Anthropic Console에서 설정한 결제 수단으로 청구됩니다.

**Q: 사용량 제한할 수 있나요?**
A: Anthropic Console에서 월간 한도를 설정할 수 있습니다.

---

## 📁 파일 구조

```
script-writer/
├── app.py              # 메인 앱 코드
├── requirements.txt    # 패키지 목록
└── README.md          # 이 파일
```
