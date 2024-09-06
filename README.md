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
<details>
<summary>2. 연산자 실습 </summary>

```C++
// 1. 숫자의 사칙연산
int ten = 10;

Console.WriteLine($"{ten + 7}");
Console.WriteLine($"{ten - 3}");
Console.WriteLine($"{ten * 2}");
Console.WriteLine($"{ten * 1.5}");
Console.WriteLine($"{ten / 3}");
Console.WriteLine($"{ten % 4}\n");

// 2. 문자의 계산
string name = "Unity-js"; // 자신의 이름, 닉네임 으로 연습해보세요.
int year = 2024;

string introduce = "안녕하세요. 제 닉네임은 \""+ name +"\" 입니다.";
string thisYear = "올해는 '" + year +"년' 입니다.";

Console.WriteLine(introduce);
Console.WriteLine(thisYear + "\n");

// 3. 논리 연산  
int tenten = 10;

bool result_1 = tenten == 10;   // tenten 이 10 이랑 같다
bool result_2 = tenten != 11;    // tenten 이 11 이랑 같지 않다
bool result_3 = tenten < 20;    // tenten 이 20 보다 작다
bool result_4 = tenten > 5;    // tenten 이 5 보다 크다

Console.WriteLine($"{result_1}, {result_2}, {result_3}, {result_4}");

// 4. 사칙연산 간 우선순위가 어떻게 될까요?
// (*, /, %) 다음 (+, -) 로 사칙연산이 이루어지나, ()를 사용할 경우 우선순위를 바꿔줄 수 있는거 같습니다.
```
# 오늘 내용 중 기억해야 할 것

2번 '문자의 계산' 을 작성할때, +로 변수 값을 넣어 줄수 있고, 따옴표와 큰 따옴표를 사용하는 방법에 대해 기억해야 할 것 같습니다. 

산술 연산 말고도 논리 연산에서의 우선 순위도 추가적으로 알아봐야 할 것 같습니다.

</details>

