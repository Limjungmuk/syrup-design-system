# Syrup Design System

디자인 시스템 Markdown 원본과 문서 웹을 함께 관리합니다.

## 폴더 구성

- `MD/`: 컴포넌트별 원본, 디자인 토큰, 피그마용 통합 가이드, 웹 제작 MD.
- `Design System/content/`: 문서와 Figma 자산의 연결 정보.
- `Design System/tools/`: MD 빌드·로컬 서버·검사 도구.
- `Design System/site/`: 웹 소스, 정적 자산, 동작 예제 소스와 생성된 JS·CSS, 공개 다운로드.

두 폴더는 형제 관계를 유지합니다. 빌드 도구는 `Design System`에서 `../MD`를 참조합니다.

## 로컬 실행

`Design System/시럽 로컬 실행.command`를 더블클릭하거나 아래 명령을 실행합니다.

```sh
cd "Design System"
python3 tools/serve.py
```

브라우저에서 http://localhost:4173 을 엽니다. 생성된 정적 파일을 포함하므로 미리보기 실행에 Node 설치는 필수가 아닙니다.

## MD 변경 후 웹 갱신과 확인

```sh
cd "Design System"
python3 -m pip install --target .tools -r tools/requirements.txt
python3 tools/build.py
python3 tools/check.py
```

원본 MD 변경 후 웹 데이터·다운로드 MD·전체 ZIP을 함께 생성하고, 변경 결과를 확인합니다. 빌드는 Figma 이미지를 자동으로 갱신하지 않습니다.

React 동작 예제의 TSX·CSS 소스는 `Design System/site/code/`에 있으며, 현재 웹에서 사용하는 생성된 번들도 포함합니다. 기존 MD 빌드는 React 번들을 다시 컴파일하지 않습니다. React 재컴파일용 프로젝트 설정은 별도 보완 대상입니다.

## Git 관리 범위

`MD/`와 `Design System/`을 관리합니다. 로컬 의존성·캐시·개인 설정·백업과 최상위의 영상·디자인 작업 폴더는 제외합니다. 제외된 파일은 PC에서 삭제하지 않습니다.

GitHub Push와 공개 사이트 배포는 별개입니다. 이 저장소 연결만으로 기존 공개 사이트의 자동 배포를 설정하지 않습니다.
