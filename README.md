# Gugudan_Game
[![JDK](https://img.shields.io/badge/JDK-15.0.2-orange)](https://pypi.org/project/dart-fss/)


랩퍼클래스와 랜덤함수를 이용한 구구단 게임

- Source code: https://github.com/parkbohyun/Gugudan_Game

``` java
import java.util.*;
import java.io.*;
```

## Source

```java
import java.util.*;
import java.io.*;

public class Gugudan_Game {
	  public static void main(String[] args) throws IOException{
		  int x, y;
		  Random r= new Random();

		  if(args.length==1){
			  x= Integer.valueOf(args[0]).intValue(); 
			  //랩퍼 클래스 intValue()는 Integer 객체로 생성된 내용 값을 int형으로 형변환
		  }else{
			  x= Math.abs(r.nextInt() % 9) + 1;
		  }
	
		  y= Math.abs(r.nextInt() % 9) + 1;
		  
		  int num= x*y;
	
		  System.out.println();
		  System.out.println("* 구구단 "+ x + "단에 대한 문제입니다");
		  System.out.println();
	
	
		  System.out.print(x +" * "+ y +" = ");
		 
		  BufferedReader in= new BufferedReader(new InputStreamReader(System.in));
		  
		  String user;
		  user= in.readLine();
	

		  int inputNum = Integer.parseInt(user);
		  //랩퍼클래스 parseInt()는 static으로 Integer 객체를 생성하지 않고, parameter로 int형으로 형변환
	
		  if(num==inputNum){
			  System.out.println("맞았습니다!");
		  }else{
			  System.out.println("틀렸습니다. 정답은 "+ num +"입니다.");
		  }
	  }
}
```

## 실행 화면
<img src = "https://user-images.githubusercontent.com/47629333/173706975-69f1fb72-7d06-4fa8-8f75-e240a1ebdca0.png" width = "70%" height = "70%">
