# th-korean-glossary

[태국 사이트 한국어](https://github.com/wotjq2/th-korean) 유저스크립트의 **검색 용어집**입니다. 모든 PC의 스크립트가 여기 `glossary.txt` 를 받아 씁니다.

- 형식: 한 줄에 `한국어=태국어`, `#` 로 시작하는 줄은 설명
- 넣는 법: 라자다·쇼피에서 **한** 버튼 → 맨 위 **검색 용어집** 칸에 적고 **저장** → 이 저장소에 바로 커밋됩니다
- 반영: 저장한 PC는 바로, 다른 PC는 10분 안에
- `@꾸밈말`: 칸 제목에 이 표시가 있는 칸(색·소재·성별·크기·냉동…)의 말은 조합할 때 상품 이름 뒤로 갑니다. `돼지막창 냉동` → `ไส้ใหญ่หมู แช่แข็ง`. 표시 없는 칸과 설정 패널에서 추가한 말은 상품 이름으로 봅니다.

## 왜 스크립트와 따로 두나

설정 패널에서 바로 저장하려고 브라우저에 GitHub 토큰을 둡니다. 그 토큰이 **이 저장소에만** 쓸 수 있게 하려는 것입니다. 토큰이 새어 나가도 바뀌는 것은 단어뿐이고, 모든 PC가 자동 업데이트로 받는 스크립트 코드는 건드릴 수 없습니다. 용어집 값은 검색어·화면 글자로만 쓰여 코드로 실행되지 않습니다. 잘못 바뀐 단어는 커밋 기록에서 되돌리면 됩니다.

토큰을 만들 때는 **Only select repositories → `th-korean-glossary`**, **Contents: Read and write** 만 주세요.

## 다른 언어 용어집 (glossary-xx.txt)

통합 번역의 입력 언어 막대(미·중·힌·스·아 …)에서 고른 언어로 한국어를 바꿀 때 쓰는 용어집입니다. 언어마다 파일 하나: `glossary-en.txt`(영어), `glossary-vi.txt`(베트남어) …

- 형식: 한 줄에 `한국어=그 언어`. 입력칸에 친 한국어 **전체**가 줄의 한국어와 같을 때만(띄어쓰기·끝 문장부호는 보지 않음) 그 값을 쓰고, 아니면 구글 번역
- 물음표로 끝나게 친 말(`얼마예요?`)은 값도 물음표(`?` `？` `؟`)로 끝날 때만 씀
- 반영: 브라우저·번역 도우미 모두 1시간 안에 (확장 업데이트·웹스토어 심사 필요 없음)
- 새 언어: 여기에 파일 하나 + th-korean 저장소 `config.json` 의 그 언어 줄에 `"glossary": "glossary-xx.txt"`
- 처음 넣은 것(2026-11-04): 21개 언어에 인사·쇼핑·식당·길 묻기 기본 말 62개 — 구글이 한국어에서 바로 옮기면 틀리는 말('깎아 주세요' → 면도, '공항' → 비행기)을 바로잡아 둠. 영어·중국어는 예전 샘플 188줄도 들어 있음

## 출처·라이선스

아래 파일에는 국립국어원 「한국어기초사전」(<https://krdict.korean.go.kr>, 2026-10-19 전체 내려받기 자료)에서 가져온 낱말이 들어 있습니다.

- `glossary-ar.txt` `glossary-en.txt` `glossary-es.txt` `glossary-fr.txt` `glossary-id.txt` `glossary-ja.txt` `glossary-mn.txt` `glossary-ru.txt` `glossary-vi.txt` `glossary-zh.txt` `glossary-th-krdict.txt`
- `reverse-ar.txt` `reverse-en.txt` `reverse-es.txt` `reverse-fr.txt` `reverse-id.txt` `reverse-ja.txt` `reverse-mn.txt` `reverse-ru.txt` `reverse-th.txt` `reverse-vi.txt` `reverse-zh.txt` — 언어 교차용 거꾸로 표. 한 줄에 `그 언어=한국어`. 한국어 쪽 뜻이 여럿인 낱말은 `reverse-xx-ko.txt` 에 따로 있고 한국어로 옮길 때만 씁니다. 영어 → 한국어는 구글 번역이 더 나아서 쓰지 않습니다(`reverse-en-ko.txt` 없음, `reverse-en.txt` 는 다른 언어로 건너갈 때만). 사전 전체에서 한국어 한 표기로만 이어지는 낱말 가운데 어느 뜻의 첫 대역어이고 짧은 말만 골랐습니다. 입력·메시지 전체가 왼쪽과 같을 때 그 언어 → 한국어, 또는 한국어를 거쳐 다른 언어로 옮기는 데 씁니다(통합 번역 1.30.1 다음 판부터, 번역 도우미의 LINE 은 먼저).
- 라이선스: 크리에이티브 커먼즈 저작자표시-동일조건변경허락 2.0 대한민국 (CC BY-SA 2.0 KR, <https://creativecommons.org/licenses/by-sa/2.0/kr/>). 위 파일들은 전체를 같은 라이선스로 배포합니다.
- 변경 사항: 동형어까지 합쳐 뜻이 하나뿐인 낱말만 골랐고, 첫 대역어만 남겼으며, 괄호·음역 표기를 손질했습니다.
- 파일 안에서 `# === 한국어기초사전 끝` 줄 위가 사전 낱말, 아래가 직접 고른 말입니다. 같은 한국어는 아래쪽이 이기므로 직접 고른 말이 우선합니다.
- `glossary.txt` 와 나머지 언어 파일에는 이 자료를 넣지 않았습니다.

### 위키낱말사전 (2026-11-11)

아래 파일의 `# --- 위키낱말사전 ---` 칸에는 영어판 위키낱말사전(Wiktionary, <https://en.wiktionary.org>)의 번역표에서 가져온 낱말이 들어 있습니다. kaikki.org 의 wiktextract 추출 자료(<https://kaikki.org>, 2026-10-01 덤프)를 썼습니다.

- 새로 채운 언어(전에는 기본 말 62개뿐): `glossary-de.txt` `glossary-pt.txt` `glossary-pl.txt` `glossary-tr.txt` `glossary-he.txt` `glossary-hi.txt` `glossary-bn.txt` `glossary-ur.txt` `glossary-ta.txt` `glossary-te.txt` `glossary-mr.txt` `glossary-yue.txt` — 언어마다 4천~2만 2천 줄
- 기초사전 칸 아래에 덧붙인 언어(기초사전에 없던 한국어만): `glossary-ja.txt` `glossary-zh.txt` `glossary-fr.txt` `glossary-es.txt` `glossary-ru.txt` `glossary-ar.txt` `glossary-en.txt` `glossary-vi.txt` `glossary-id.txt` `glossary-mn.txt`
- 태국어: `glossary-th-krdict.txt` 의 기초사전 칸 아래에만 넣었습니다(`glossary.txt` 에 있는 한국어와 쇼핑 뜻이 먼저인 함정 말은 뺌). `glossary.txt` 는 그대로입니다.
- 흔한 말인데 번역표의 뜻이 엇나간 한국어 220여 개는 모든 언어에서 뺐습니다(가자=Gaza, 지난=Jinan, 해주=Haeju, 그린=putting green, 픽업=pickup truck, 괜찮아요=you're welcome 같은 것). 이런 말은 구글 번역으로 갑니다.
- 지은이: Wiktionary 기여자들. 라이선스: 크리에이티브 커먼즈 저작자표시-동일조건변경허락 4.0 국제 (CC BY-SA 4.0, <https://creativecommons.org/licenses/by-sa/4.0/>). 위키낱말사전 칸은 같은 라이선스로 배포합니다. 같은 파일의 기초사전 칸은 위의 CC BY-SA 2.0 KR 그대로입니다.
- 변경 사항: 영어 낱말의 뜻 하나에 달린 번역표에서 한국어와 그 언어 값을 짝지었습니다. 기초사전에서 뜻이 여럿인 한국어, 기초사전과 뜻이 다른 표(한자가 다른 동음어), 사투리·옛말·지역 꼬리표 값은 뺐고, 모음 부호·강세 표시를 걷어 냈으며, 여러 표에 나오는 한국어는 모든 표에 공통인 값만 남겼습니다. 파일에 이미 있던 한국어는 넣지 않아 기초사전·직접 고른 말이 그대로 이깁니다.
- 위키낱말사전 칸도 `# === 한국어기초사전 끝` 줄 위에 있어, 번역 도우미의 화면 번역(거꾸로 찾기)에는 쓰이지 않습니다.
- 품질(가려서 잰 것): 표본 480개 중 구글 번역과 같음 206, 차이 없음 109, 사전이 나음 98, 구글이 나음 61, 둘 다 틀림 6. 영어·베트남어·인도네시아어·몽골어·태국어 표본 150개: 같음 75, 차이 없음 29, 사전이 나음 31, 구글이 나음 13, 둘 다 틀림 2. `glossary-th-krdict.txt` 는 `glossary.txt` 에 없는 태국어 낱말만 따로 모은 것으로, 통합 번역 1.30.1 다음 판부터 `glossary.txt` 로 다 못 옮긴 검색어·입력칸의 말이 통째로 여기 있을 때 씁니다(메신저 제외).
