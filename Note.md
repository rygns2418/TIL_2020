### 컴퓨터가 변수를 처리하는 방법



- 메모리 공간 분류

1. 코드영역 : 소스코드
2. 데이터영역 : 전역, 정적변수
3. 힙영역 : 동적할당 변수
4. 스택영역: 지역, 매개변수



### 동적메모리할당

*  C는 malloc() 함수를 이용해 메모리 공간 확보 가능

* malloc() 함수는 메모리 할당에 성공하면 주소를 반환, 실패시 NULL 반환

* stdlib.h에 정의

* 동적으로 할당된 변수는 free()로 메모리 해제를 해줘야됨

* string.h에 정의된 memset() 함수로 특정값으로 메모리 초기화 가능

  * memset(포인터변수, 초기화할 값, 크기);

    ``` cpp
    char *a = malloc(100);
    memset(a,'A',100);
    ```

### 파일 입출력

* 파일입출력 변수는 FILE 형식 포인터 변수로 선언

* 파일열때는 fopen(), 닫을때는 fclose()

  ``` c++
  FILE *fp;
  fp = fopen(파일 경로, 접근방식);
  fclose(fp);
  ```

* 파일 열기(fopen) -> 파일 읽기/쓰기(fprintf, fscanf) -> 파일 닫기(fclose)



* 접근방식 종류 :
  * r : 파일에 접근하여 데이터 읽음
  * w : 파일에 접근해서 데이터 기록 (덮어쓰기)
  * a : 파일에 접근하여 데이터를 뒤에서부터 기록
* 파일 입출력함수 :
  * fprintf(파일포인터, 형식지정자, 변수);
  * fscanf(파일포인터, 형식지정자, 변수);



