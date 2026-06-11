# issamGPT 견적서 생성기

issamGPT 견적서 입력 화면을 Vercel에서 열 수 있도록 만든 정적 웹앱입니다.

## 중요한 구조

- Vercel은 화면만 호스팅합니다.
- 실제 XLSM/PDF 생성은 회사 PC에서 실행 중인 `quote_web_agent.py` 로컬 생성기가 처리합니다.
- 로컬 생성기는 `Z:` 드라이브의 견적서 템플릿과 Windows Excel을 사용합니다.

## 로컬 생성기 실행

회사 PC에서 아래 파일을 실행합니다.

```powershell
.\quote_web_agent_start.cmd
```

또는 Python으로 직접 실행합니다.

```powershell
python .\quote_web_agent.py
```

로컬 주소는 `http://localhost:8787/issamgpt` 입니다.

## Vercel 배포

이 저장소를 GitHub에 올린 뒤 Vercel에서 Import 하면 됩니다.

- Framework Preset: `Other`
- Build Command: 비워두기
- Output Directory: `public`

배포된 링크에서 버튼을 쓰려면 같은 PC에서 로컬 생성기가 켜져 있어야 합니다.
