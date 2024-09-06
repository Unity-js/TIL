# TIL

C# TIL을 업로드 하는 공간입니다.

<details>
<summary>1. 데이터 다루기 실습 </summary>

  ```C++
// 1. 변수 만들기
// 2. 변수에 데이터 넣기
int level = 1;
int count = 2;

float persentage = 50.0f;
float speed = 10.0f;

string nickname = "name";
string description = "text";

// 3. 형변환하기 숫자-숫자
int iTen = 10;
float fTen = iTen; // iTen 을 저장해보세요

float fFive = 5.5f;
int iFive = (int)fFive; // fFive 을 저장해보세요


// 4. 형변환하기 숫자-문자
int n = 10;
float f = 0.5f;

string textn = n.ToString();
string textf = f.ToString();

// 5. 형변환하기 문자-숫자
string strTen = "10";
string strSix = "6.2";

int ten = int.Parse(strTen);
float six = float.Parse(strSix);

// 6.### Convert 와 Parse 는 어떤 차이가 있는지 설명해주세요.
// 둘 다 자료형의 변환이 일어난다는 점은 비슷하지만, null 값을 변환 시킬때 Convert의 경우 0을 반환하게 되지만, Parse의 경우 예외처리가 일어납니다.
```

# 오늘 내용 중 기억해야 할 것

Convert와 Parse 의 차이점, 그로 인해 각자 어떤 상황에서 사용 해야 할지 기억 해야 할 것 같습니다.

Convert 의 경우, float 값을 int 로 변환 시키면 반올림이 일어남

parse 의 경우 String형에서 사용 가능

</details>
