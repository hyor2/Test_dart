# Test_dart
study https://www.youtube.com/watch?v=3Ck42C2ZCb8&list=PLmEhRs1HB7RHX6VbXslXLRYH3HK0fm_Lj&index=29
# 1. variables declaration
  타입 변수명 = _____ ;
  
  print('$ {name} ${name2}); 
  print('$name $name2); 
  
  -> 변수가 하나일 때 중괄호 생략 가능, python의 %d,%s 등과 기능 유사
  
  String name='레드벨벳';
  
  Stirng name='슬기';
  
  print('${name.runtimeType} $ {name2} );
  
  print( '$name.runtimeType $name2' );    
  
  
  출력>>> String 슬기
      레드벨벳.runtimeType 슬기
  
  함수에서는 {}사용해야함, runtimeType함수는 빌드할 때의 타입을 알려줌

      
  
# 2 var vs dynamic type
  -> 지동으로 타입 유추
  
  dynamic name = '레드벨벳';
  var num = 1;
  
  dynamic, var 모구 여러 타입 선언 가능
  var 타입은 선언하는 순간 고정되어 타입 변경 불가
  dynamic은 변경가능
  
  name=1;    
  num='레드벨벳';     //error
  
 
 # 3 nullable vs non-nullable
  모든 타입은 null 값도 들어갈 수 있는 것과 없는 것으로 나뉨
  
  String name = '코드팩토리';
  
  // name = null;       error
  
  String? name2 = '블랙핑크;
  
  name2=null;         //가능
  
  String? name3 = '레드벨벳';
  
  print( name3! );    //null이 들어갈 수 있지만 null이 아님을 명시
 
 
 # 4 Final vs Const keyword
  -> 한 번 선언하면 변경 불가
  
  var keyword 생략 가능 ex) final nmae = "____";
  
  final은 빌드 타임에 값을 알지 않아도 됨
  
   const는 빌드 타임에 값을 알아야함. -> 빌드 하기전에 값이 있어야 함
 
  final DateTime now = DateTime.now();
  
  //Const DateTime now2 = DateTime.now();     error
  
 
  // DateTime.now()는 코드가 실행되는 순간의 시간을 반환-> 빌드 이후 
# 5 null 조건 오퍼레이터

  double? number=4.0;
  number=null;
  number?? =3.0;
  
  -> ?? operator : number가 null일 때 오른쪽 값으로 바꿔라
  
  type비교 오퍼레이터
  
  print(number is int);
  print(number is! int);
  
# 6 List type

  List <타입> 변수= [ , , , ];
  ex) List <int> numbers = [1,2,3,4,5];
  
  print(numbers.length);
  numbers.add(3);      //맨 끝에 추가
  numbers.remove(3);   //중복 있을 시 맨 앞부터 제거
  numbers.indexOf(4);  //4의 인덱스를 알 수 있음
  
  print( numbers );
  >>> [1,2,4,5,3]
  
# 7 map
   python의 딕셔너리와 유사 -> key, value값 가지고 있음
   Map< String, String> 변수 = { 'key1' : 'value1', 'key2' : 'value2' };
   //key와 value의 타입을 적어줌
   //key, value값 추가
   Map<String, bool> isHarryPotter={'Harry' : true, 'Ron' : true};
   isHarryPotter.addAll( 'spiderman' : false)
   isHarryPotter['Halk']=false;
   //제거
   isHarryPotter.remove('Harry{Potter');
   //key값 모두 출력 -> python과 유사
   print(isHarryPotter.keys);
   //value값 모두 출력
   print(isHarryPotter.values);
  
# 8 set
  중복값 X
  final set <String> names={'Flutter', 'Python', 'Cpp'};
  names.add('__');
  names.remove('___');
  names.contains('Flutter');    //값이 set에 존재하는지 확인
 
# 9 if문, switch문
  -> c++과 동일
  
# 10 Loops
  for loop, do while, break, continue -> c++과 동일
  
  //python과 유사
  List <int> numbers=[1,2,3,4,5,6];
  for(int number in numbers)
  {
    print(numbers);
  }
  
# 11 enum 
  enum Status
  {
    append.
    pending,
    rejected,
  }
  -> cpp와 다르게 내부에서 int로 저장되지 않음
    
    enum Status
    {
      APPENDING,
      PENDING,
      REJECTED,
    }
    enum Status2
    {
     APPENDING2,
     PENDING2,
      REJECTED2,
     REJECTED2,
    }
    void main() 
    {
     Status status=Status.PENDING;
      Status2 status2=Status2.PENDING2;
  
      if(status==status2)
      {
        print("동일");
      }   
      else
        print("다름");
    }
    
   >>> cpp에 경우에는 동일이 출력되고, dart에서는 다름이 출력됨
 # 12 함수 선언
  타입 함수명()
  {
  }
  -> 타입이 void일 때는 생략 
