---
share: true
title: index-python 오답노트
---

# index-python 오답노트
created: 2022-10-06
last modified: 


## 사용자 입력

- input으로 입력받은 여러 숫자(공백으로 구분)를 수치형으로 일괄 변환: `map(자료형, input().split())`
- map( function, iterable ) -> [자세한 설명](https://dojang.io/mod/page/view.php?id=2286)


## 산술 연산

- 나눗셈 몫을 정수로 출력(나눗셈 결과값보다 작은 정수 중에서 가장 큰 정수): - `//` 연산자 사용. 4/3 -> 1.3333 | 4//3 -> 1
- 문자열 크기 비교는 ASCII 번호 순: 소문자 < 대문자


## 문자열

- 문자열 -> 아스키코드: `ord('A')` -> 65
- 아스키코드 -> 문자열: `chr(48)` -> '0' (수치형 문자 0)
- 역순으로 출력(간격을 음수로 지정): `'hello'[::-1]`  -> 'olleh'
- 'abc'의 각 문자 사이에 쉼표 입력: `','.join('abc')` -> 'a,b,c' 
- '입력값'.join(자료): 점(.)왼쪽에 있는 요소를 .join(자료)의 자료 인덱스 사이사이에 입력
- `find()` 함수는 없으면 -1 반환. `index()` 함수는 없으면 ValueError 반환
- `문자열.split()` => list 반환


## 딕셔너리

- [[Dictionary Methods List]]
- dict -> list: key만 리스트로 변환
- 딕셔너리에 없는 키로 조회해도 에러 나지 않도록 하기: `딕셔너리.get('key')`
- 하나 이상의 key:value 추가: `딕셔너리.update(딕셔너리 or 딕셔너리 형태 리스트)` 


## 콘솔 입출력

- print() 출력할 때 쉼표(,)를 붙이기: `print( variable, end = ', ' )`
- print() 소수점 3자리까지 출력: `print('%0.3f' % 숫자 또는 변수)` or `print(f'{숫자 또는 변수:.3f}')`
- print() % 표시(소수점 2자리): `print(f'{숫자 또는 변수:.2%}')`
- `#!`([[셔뱅]]) => 파일을 실행파일로 바꾸기
- [[Makefile]]: Makefile에 테스트 코드를 넣으면 $ make test 명령으로 테스트 코드 실행
- [[argparse]] 모듈 사용해 프로그램에 인수 전달


## 날짜

- [시간 관련 함수 설명](https://python.bakyeono.net/chapter-11-3.html)
- [strftime 시간 표시 형식](https://strftime.org/)
- 시, 분만 날짜 형식으로 지정하기: `time.time(시간, 분)` -> datetime 객체 반환 -> 더하기 빼기 안 됨
- 10시 30분에서 40분 후의 시, 분 표시하기: `( datetime.datetime(연, 월, 일, h, m) + datetime.timedelta(minutes=s) ).strftime("%H:%M")` -> 연, 월, 일은 그럴듯한 값으로 아무 거나 입력(eg. 100, 1, 1)
- 시, 분 표시를 한 자리 시각은 한 자리로 두 자리 시각은 두 자리로 표시(strftime): `strftime("%-H %-M")`


## 변수

- [[shallow_copy-deep_copy]]


## 코드 스타일 및 오류 확인

- `$ flake8 파일명` 
- `$ pylint 파일명`
- `$ black 파일명` 
- `$ yapf -i 파일명`: i는 덮어쓰기


## 개념

- [[GIL]]
- 