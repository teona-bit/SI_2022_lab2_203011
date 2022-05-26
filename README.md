Втора лабораториска вежба по Софтверско инженерство

Теона Данева, 203011

Control Flow Graph


![CFG](https://user-images.githubusercontent.com/52212878/170599991-1537b68f-7a0c-4127-a500-8cb3b56e82a9.png)

Цикломатска комплексност


Цикломатската комплексност може да се определи на 3 начини и на сите 3 начини цикломатската комплексност изнесува 3.

	1. Број на предикатни јазли + 1 -> 8 предикатни јазли + 1 = 9
	2. Број на региони -> 9 региони
	3. Број на ребра - број на јазли + 2 = 31 - 24 + 2 = 9 
  
  Тест случаи според критериумот Every statement
  
  
  Потребни се 3 тест случаи да се покрие секоја линија од кодот.

	1. List[] -> фрла исклучок "List length should be greater than 0". Ги покрива јазлите 1, 2, 24
	2. List["0", "#", "0"] -> фрла исклучок "List length should be a perfect square". Ги покрива јазлите 1, 3, 4, 5, 6, 24
	3. List["#", "0", "#", "0", "#", "0", "#", "0", "#"] -> ги покрива сите останати јазли 1, 3, 4, 5, 7, 8.1, 8.2, 8.3, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19,
     20,21, 22, 23, 24
	
	
	Тест случаи според критериумот Every branch
	
	
	За да се поминат сите гранки во кодот се потребни 3 тест случаи. Истите тест случаи кои ја покриваат секоја линија од кодот, ги покриваат и сите гранки во           кодот.
	
	1. List[] -> фрла исклучок "List length should be greater than 0". Ги покрива гранките 1-2, 2-24
	2. List["0", "#", "0"] -> фрла исклучок "List length should be a perfect square". Ги покрива гранките 1-3,4, 5-6, 6-24
	3. List["#", "0", "#", "0", "#", "0", "#", "0", "#"] -> ги покрива сите останати гранки 1-3,4 5-7, 7-8.1, 8.1-8.2, 8.2-23, 23-24, 8.2-9, 9-21,22, 21,22-8.3,            8.3-8.2, 9-10, 10-11, 11-12, 12-13, 13-16, 12-14, 14-15, 15-16, 11-16, 16-18, 18-19, 19-20, 18-20, 20-8.3, 16-17, 17-18 


       Објаснување на напишаните unit tests

       Тестовите се напишани во src/test/java/SILab2Test. Во двете функции everyStatementTest и everyBranchTest со помош на 3 тест случаи се тестираат сите линии и        гранки од кодот.
       Тестот започнува со анотацијата @Test. Линиите 1, 2, 5, 6 од кодот се тестираат со помош на методата assertThrows бидејќи фрлаат исклучок и со методата
       assertTrue се проверува дали е фатен соодветниот исклучок. Со методата assertEquals се споредува резултатот кој го посакуваме и добиениот резултат од функциј
