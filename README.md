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
<details>
<summary>3. 본격 프로그래밍 시작해보기 </summary>

```C++
// 1. 입력받은 데이터가 숫자인지 문자열인지 판단

using System.ComponentModel;

string input = Console.ReadLine();

int a;

bool logic = int.TryParse(input, out a);

if (logic)
{
    Console.WriteLine("숫자입니다.");
} else
{
    Console.WriteLine("문자열입니다.");
}

//2.입력받은 데이터가 숫자인지 문자열인지 불리언인지 판단

string input2 = Console.ReadLine();

int b;
bool c;

if (c = int.TryParse(input2, out b))
{
    Console.WriteLine("숫자입니다.");
} 

else if (c = bool.TryParse(input2, out c))
{
    Console.WriteLine("불리언입니다.");
}
else
{
    Console.WriteLine("문자열입니다.");
}

// 3. 입력받은 데이터가 숫자라면 100 보다 큰지 작은지 알려주는 프로그램 만들기

string input3 = Console.ReadLine();

int d;

bool logic2 = int.TryParse(input3, out d);

if (!logic2)
{
    Console.WriteLine("숫자가 아닙니다.");
}
else
{
    if (d >= 100)
    {
        Console.WriteLine(d + "은(는) 100 보다 같거나 큰 수 입니다.");
    }
    else
    {
        Console.WriteLine(d + "은(는) 100 보다 작은 수 입니다."); 
    }
}

// 4. 입력받은 데이터가 숫자라면 짝수인지 홀수인지 알려주는 프로그램 만들기

string input4 = Console.ReadLine();

int f;

bool logic3 = int.TryParse(input3, out f);

if (!logic3)
{
    Console.WriteLine("숫자가 아닙니다.");
}
else
{
    if (f % 2 == 0)
    {
        Console.WriteLine(f + "은(는) 짝수 입니다."); 
    }
    else if (f % 2 != 0)
    {
        Console.WriteLine(f + "은(는) 홀수 입니다.");
    }
}

// 5.  언제 if 를 쓰고 언제 case 를 쓸까요?
// 조건이 상수가 아닌 연산이거나 변수일때 if , 상수 값일때 case를 사용해야 할 것 같습니다.
```

# 오늘 내용 중 기억해야 할 것

case를 사용하면 break 를 사용 해 주어야 하고, case 의 조건을 상수 값으로 두어야 한다는 것 , 따라서 다음 case 조건에는 이전에 사용했던 상수를 사용 할 수 없음

else if 에 비해 case 의 경우 조건식을 전부 계산하지 않기 때문에 처리속도가 더 빠르지 않을까 싶습니다.

코드가 지저분해서 간소화 시키는 연습을 해야 할 것 같습니다.

* 위에 "숫자" 는 정수에 한정해서 작성했습니다, 소수가 입력 되었을 때에도 문자가 아닌 숫자로 판단할 수 있게 더 공부 해야 할 것 같습니다.

</details>
