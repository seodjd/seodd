Q1.

해당 문제에서 5의 값을 출력하기 위해 var3에서 2.5가 출력되길 기대했을 것이다.
하지만 var1과 var2는 int타입으로 연산값이 2.5일 경우 2를 출력한다.
그 결과 2 * var2로 연산되어 값이 4로 출력된 것이다.

원하는 값이 나오게 하기 위해서 수정해 보자면

방법1. double var3 = (double)var1/var2;
방법2. double var3 = var1/(double)var2;
방법3. double var3 = (double)var1/(double)var2;

등 타입 변환을 해줘야 한다.

Q2.

int x=10;
int y=20;
int z = (++x) + (y--);
System.out.println(z);

증감연산자는 변수값을 1씩 증가 혹은 감소시키는 연산자이다.
이 문제를 풀기 위해서 추가로 알아야 할 것은 증감연산자의 전위형과 후위형이다.
전위형의 경우 우선 변수값을 1 증가 또는 감소를 시킨 후 다른 연산자를 처리하는 반면,
후위형의 경우 다른 연산자 처리 후 변수값를 증가 또는 감소시킵니다.

문제를 보자면 변수 z에서 ++y는 전위형 y--는 후위형으로 
int z = (11) + (20)	이 됩니다.

그렇기에 출력되는 결과값은 31이라는 결론을 도출할 수 있습니다.

Q3.

        while (true) {

            int dice1 = (int) (Math.random() * 6) + 1;
            int dice2 = (int) (Math.random() * 6) + 1;
        
            System.out.println("(" + dice1 + ", " + dice2 + ")");
            if ((dice1 + dice2) == 5) {
                break;
            }
        }	
