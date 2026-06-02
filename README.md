# GPU Programming Project

상명대학교 GPU 프로그래밍 수업 팀 프로젝트

OpenGL을 활용하여 텍스처가 적용된 3D 실내 공간을 구현한 프로젝트입니다.

## 프로젝트 개요

본 프로젝트는 C++과 OpenGL을 이용하여 3차원 실내 공간을 렌더링하는 프로그램입니다.

GLFW를 사용하여 윈도우 생성 및 입력 처리를 수행하고, GLAD를 통해 OpenGL 함수를 로드하였으며, GLM 라이브러리를 이용해 카메라 이동 및 행렬 연산을 구현했습니다.

또한 Vertex Shader와 Fragment Shader를 활용하여 텍스처가 적용된 벽, 바닥, 천장을 렌더링하였습니다.

## 발표자료

발표자료 삽입

## 개발 환경

### Language
- C++

### Graphics API
- OpenGL 3.3 Core Profile

### Libraries
- GLFW
- GLAD
- GLM
- stb_image

### Development Tool
- Visual Studio

## 주요 기능

### 3D 공간 렌더링
- 바닥(Floor)
- 천장(Ceiling)
- 앞벽(Front Wall)
- 뒷벽(Back Wall)
- 좌측 벽(Left Wall)
- 우측 벽(Right Wall)

### 텍스처 매핑
- 각 면에 텍스처 이미지 적용
- 이미지 로딩을 위한 stb_image 사용

### 카메라 시스템
- FPS 방식 카메라 이동 구현
- View Matrix 적용

### 사용자 입력 처리

#### 키보드 이동
| 키 | 기능 |
|------|------|
| W | 전진 |
| S | 후진 |
| A | 좌측 이동 |
| D | 우측 이동 |
| ESC | 종료 |

#### 마우스
- 시점 회전

#### 스크롤
- 줌 인 / 줌 아웃

---

## 프로젝트 구조

```text
GPUProgramming
│
├── include
│   ├── glad
│   ├── GLFW
│   └── glm
│
├── libs
│
├── resources
│   └── textures
│
├── shader
│   ├── wall.vs
│   ├── wall.fs
│   └── 2.stencil_single_color.fs
│
├── src
│   ├── glad.c
│   └── main.cpp
│
├── GPUProgramming.sln
├── GPUProgramming.vcxproj
└── README.md
```

---

## 구현 내용

### OpenGL 초기화
- GLFW 초기화
- OpenGL Context 생성
- GLAD 로딩
- Depth Test 활성화

### Shader
- Vertex Shader
- Fragment Shader

Shader를 통해 MVP(Model-View-Projection) 변환을 수행하고 텍스처를 출력합니다.

### Texture
- 이미지 파일 로드
- OpenGL Texture 객체 생성
- Texture Coordinate 적용

### Camera
- Keyboard Input 처리
- Mouse Movement 처리
- Scroll Input 처리

---

## 실행 방법

### 1. 프로젝트 클론

```bash
git clone https://github.com/hxtchhxkxr/GPUprogramming.git
```

### 2. Visual Studio 실행

```text
GPUProgramming.sln
```

열기

### 3. 빌드

```text
Build → Build Solution
```

### 4. 실행

```text
Ctrl + F5
```

---

## 사용 기술

| 기술 | 설명 |
|--------|--------|
| OpenGL | 3D 그래픽 렌더링 |
| GLFW | Window 및 Input 처리 |
| GLAD | OpenGL 함수 로더 |
| GLM | 수학 연산 라이브러리 |
| stb_image | 이미지 로딩 |
| GLSL | Shader 작성 |

---

## 학습 내용

본 프로젝트를 통해 다음 내용을 학습하였습니다.

- OpenGL 렌더링 파이프라인
- VAO / VBO 사용 방법
- Shader 프로그래밍
- Texture Mapping
- Camera 구현
- Model / View / Projection Matrix
- 사용자 입력 처리
- 3D 공간 렌더링

---

## 프로젝트 결과

텍스처가 적용된 실내 공간을 OpenGL 환경에서 렌더링하고 사용자가 직접 이동하며 공간을 탐색할 수 있는 3D 프로그램을 구현하였습니다.
