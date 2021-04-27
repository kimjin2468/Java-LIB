# Java-LIB
My Java library

//D-day 계산하는 코드

  	int sYear =2021;      
  	int sMonth =4;        //  이곳에 오늘기준의 년,월,일을 입력 (현재 2021.04.27일로 입력되어있음)
  	int sDay =27;         
	
	int eYear =2020;      
	int eMonth = 4;       // 이곳에 비교하려는 날의 년,월,일을 입력 (2020.04.04일로 입력되어있음)
	int eDay =4;          
	
	Date sd = new Date();
	Date ed = new Date();
	
	sd.setYear(sYear);
	sd.setMonth(sMonth-1);
	sd.setDate(sDay);
	
	ed.setYear(eYear);
	ed.setMonth(eMonth-1);
	ed.setDate(eDay);
	
	long temp = (sd.getTime() - ed.getTime()) / (1000L *60L * 60L*24L);
	
 	 int diff =(int)temp;            //D-day를 담을 변수
	
	System.out.println(diff);       //결과값:388    (2021.04.27일은 2020.04.04일로부터 388일이 경과됨. )
	
