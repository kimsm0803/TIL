# MarkDown

## **(1) 마크다운이란?**

- 일반 텍스트 기반의 경량 마크업 언어

- 마크업과 반대 개념이 아니라, 마크업을 더 쉽고 간단하게 사용하고자 만들어졌습니다.

- <span style="color:red">`.md`</span>확장자를 가지며, 개발과 관련된 많은 문서는 마크다운 형식으로 작성되어 있습니다.

- 개발 분야에 있어서 <span style="color:red">`문서화`</span>는 굉장히 중요한 능력이므로 마크다운은 그 토대가 될 것입니다.

  ---



## **(2) 마크다운 문법**

### 	1. **제목 (Headings)**

- <span style="color:red">`h1~h6`</span>에 해당하는 제목을 표현합니다.

- <span style="color:red">`#`</span>을 사용합니다.

- 작성

  ```bash
  # 제목 1 
  ## 제목 2
  ### 제목 3
  #### 제목 4
  ##### 제목 5
  ###### 제목 6
  ```

---



### 2. **목록 (List)**

- 순서가 없는 목록과 순서가 있는 목록을 표현합니다.

- 순서가 없는 목록은 <span style="color:red">`- * +` </span>를 사용합니다.

- 순서가 있는 목록은 <span style="color:red">`1. 2. 3.`</span> 과 같은 숫자를 사용합니다.

- `tab 키`를 이용해서 들여쓰기를 할 수 있습니다.

- 작성

```bash
- 순서가 없는 목록
	- 서브 목록 
	- 서브 목록 

+ 순서가 없는 목록
	+ 서브 목록
	+ 서브 목록
   
* 순서가 없는 목록
	* 서브 목록
	* 서브 목록 

1. 순서가 있는 목록 
	1. 서브 목록 
	2. 서브 목록 

1. 혼합 해보기 1 
	- 순서 없음 
	+ 순서 없음 
	* 순서 없음 

2. 혼합 해보기 2 
	1. 순서 있음 
	- 순서 없음 
	2. 순서 있음
```

---



### 	3. **강조 (Emphasis)**

- 글자의 스타일링을 표현합니다.

1. *기울임* : <span style="color:red">`*기울임*` 혹은 `_기울임_` </span>
2. **굵게** : <span style="color:red">`**굵게**` 혹은 `__굵게__`</span>
3. ~~취소~~ : <span style="color:red">`~~취소~~`</span>

---



### 	4. **코드 (Code)**

- 한 줄 코드인 인라인 코드와 여러 줄 코드인 블록 코드로 나눌 수 있습니다.

1. 인라인(Inline) 코드: <span style="color:red">```inline code``</span>처럼 백틱(`)을 통해 코드를 감싸줍니다.
1. 블록(Block)코드: <span style="color:red">````python`</span> 처럼 백틱을 3번 입력하고 코드의 종류를 작성합니다.

````python
```python
for i in range(10):
    print(i)
```
````

---



### 	5. **링크 (Links)**

- 클릭하면 해당 주소로 이동할 수 있는 링크를 표현합니다.

- <span style="color:red">`[표시할 글자](이동할 주소)`</span>형태로 작성합니다.

- 작성

  `[GOOGLE](https://google.com)`을 눌러서 구글로 이동하세요.

  [GOOGLE](https://google.com)을 눌러서 구글로 이동하세요.

---



### 	6. **이미지 (Image)**

- 마크다운 문서에 이미지를 삽입할 수 있습니다.

- <span style="color:red">`![대체 텍스트](이미지 주소)`</span>형태로 작성합니다.

- `대체 텍스트`란 이미지를 정상적으로 불러오지 못했을 때 표시되는 문구입니다.

- Typora에서는 이미지 파일을 끌어와서 놓아도 자동 업로드 됩니다.

- 작성

  Git 로고입니다.

  `![Git로고](https://git-scm.com/images/logo@2x.png)`

    ![Git로고](https://git-scm.com/images/logo@2x.png)

---



### 	7. **인용 (Blockquote)**

- 주석이나 인용 문구를 표현합니다.

- <span style="color:red">`>`</span>를 사용합니다. 갯수에 따라 중첩이 가능합니다.

- 작성

  `>인용문을 작성합니다.`

  > 인용문을 작성합니다.

---



### 	8. **표 (Table)**

- 테이블(표)를 생성합니다.

- <span style="color:red">`파이프( | )`와 `하이픈( - )`</span>을 이용해서 행과 열을 구분합니다.

- 테이블 양쪽 끝의 <span style="color:red">`파이프 ( | )`</span>는 생략 가능합니다.

- 헤더 셀을 구분할 때는 <span style="color:red">`3개 이상의 하이픈 ( - )`</span>이 필요합니다.

- Typora에서는 <span style="color:red">`ctrl + T` </span>를 통해서 쉽게 표 생성이 가능합니다.

- 행을 늘릴 때는 <span style="color:red">`ctrl + enter`</span>를 누릅니다.

- 작성

  | 동물   | 종류   | 다리 개수 |
  | ------ | ------ | --------- |
  | 사자   | 포유류 | 4개       |
  | 닭     | 조류   | 2개       |
  | 도마뱀 | 파충류 | 4개       |

---



### 	9. **수평선 (Horizontal Rule)**

- 구분 선을 생성합니다.

- <span style="color:red">'- * _ '</span>을 3번 이상 연속으로 작성합니다.

  `---`

  ---
