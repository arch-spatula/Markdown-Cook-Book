# Markdown-Cook-Book

마크다운을 다루는 방법을 알려주는 리포입니다. VScode에서 작성하고 있다고 가정하고 있습니다.

검색해서 찾아보면 되는데 왜 정리하냐고요? 지난주 검색한 거 또 검색하고 싶나요? 아니면 리포 브라우저로 펴놓고 `cmd` + `f`로 해결하고 싶나요? 

물론 가끔 없는 내용도 없을 것입니다. 그때 검색하고 여기에 추가하고 정리하면 검색 빈도가 줄어들지 않을까요?

# Heading

```markdown
# h1 제목
## h2 제목
### h3 제목
#### h4 제목
##### h5 제목
###### h6 제목
```

VScode 상단을 확인해보면 마크다움 Heading으로 목차를 쉽게 돌아다닐 수 있습니다.

# 주석을 추가하는 방법

```md
<!-- 마크다운 주석 -->
```
놀랍게도 HTML 주석과 동일합니다. 문서 자체도 설계하고 교정, 피드백에 활용할 수 있습니다.

# 인용문

> Failing to plan is planning to fail
>
> — Benjamin Franklin

```md
> (인용문)
```

# 코드
블럭으로 작성하는 법입니다. 마크다운으로 설명하기 조금 어럽습니다.

```
```언어
```

이렇게 코드블럭을 시작합니다. ` ```언어`에서 `언어`만 빼면 블럭이 종료입니다.

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, World.")
}
```
생각보다 다양한 언어를 지원합니다. 이런 코드블럭을 작성하는 것으로 코드 컨벤션 같은 것을 정리할 수 있습니다.

# 이미지

마크다운에서는 html처럼 `<video />` 태그를 따로 지원해주고 있는 것은 아닙니다.


```md
<p align="center">
<img src="./img/Soyjak_Meme_Javascript.png" width="400px">
</p>
```
이미지는 이런식으로 추가할 수 있습니다.

```
![이미지](../img/img.jpeg)
```
이런식으로도 추가가 가능합니다.

# mermaid

문서에 코드로 차트를 빠르게 그릴 때 유용한 기능입니다.

[mermaid에서 지원하는 공식 문서](https://mermaid-js.github.io/mermaid/#/)

로컬에 저장하고 있으면 따로 드레그앤 드롭 방식으로 이미지를 추가할 수 있습니다.



```
bierner.markdown-mermaid
```
이 extensions을 설치하면 이제 mermaid를 미리볼 수 있습니다.


# 표
```md
|기본값|왼쪽 정렬|가운데 정렬|오른쪽 정렬|
|---|:---|:---:|---:|
|내용 1|내용 2|내용 3|내용 4|
|내용 5|내용 6|내용 7|내용 8|
|내용 9|내용 10|내용 11|내용 12|
```

|기본값|왼쪽 정렬|가운데 정렬|오른쪽 정렬|
|---|:---|:---:|---:|
|내용 1|내용 2|내용 3|내용 4|
|내용 5|내용 6|내용 7|내용 8|
|내용 9|내용 10|내용 11|내용 12|

이런식으로 표를 작성할 수 있습니다.


# 각주

이런식으로 주석을 달 수 있습니다.<sup>[2](#footnote_2)</sup>




각주는 글의 앞 부분 뒷 부분 작성하는 법 모두 알아야 합니다.

```md
내용<sup>[1](#주석이름)</sup>
```
이런식으로 글 앞은 이렇게 표시합니다.

```md
<a name="주석이름">1</a>: 내용
```

글 뒷부분은 이렇게 표시합니다.


# 범위를 초과하지만 VScode를 편하게 다루기

## 일시키는 법
https://www.youtube.com/shorts/_vNt04DimtU

## 이미지를 옆 폴더에서 드레그 앤 드롭으로 추가할 수 있습니다.

## 목차이동

https://www.youtube.com/shorts/_5EviVsd0Xo

## Math

프론트엔드 엔지니어가 px를 rem으로 변환하는 경우가 많이 있습니다. 예전에 같이 일했던 로아 좋아하던 개발자분은 [암산](https://www.youtube.com/watch?v=8dE4mRlBP5M)으로 해결했니다.

Emmet: evaluate math expression<sup>[3](#footnote_3)</sup>으로 계산을 처리할 수 있습니다.

예를 들어
```CSS
.R-24{
    border-radius: 24/16rem;
}
```

여기 코드에서 24/16을 드레그하고 Emmet: evaluate math expression를 실행하면 아래처럼 바뀝니다.

```CSS
.R-24{
    border-radius: 1.5rem;
}
```


<!-- 글 뒷 부분에 -->



<a name="footnote_1">1</a>: [여기 링크를 참고했습니다.](https://lynmp.com/ko/article/title/markdown-table-om811c9dc5oi)

<a name="footnote_2">2</a>: [여기 링크를 참고했습니다.](https://lynmp.com/ko/article/nu86c16d8f09c9fbd8)

<a name="footnote_3">3</a>: 출처: [No calculator required - VScode - Youtube](https://www.youtube.com/shorts/dCsmH5BfpdQ)
