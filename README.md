于永辉 2019310202 计192
实验三 学生选课模拟系统

实验目的：
  初步了解分析系统需求，从学生选课角度了解系统中的实体及其关系，学会定义类中的属性以及方法；
掌握面向对象的类设计方法（属性、方法）；
掌握类的继承用法，通过构造方法实例化对象；
学会使用super()，用于实例化子类；
掌握使用Object根类的toString（）方法,应用在相关对象的信息输出中。

实验要求：
1.编写上述实体类以及测试主类（注意类之间继承关系的适用）
2.在测试主类中，实例化多个类实体，模拟学生选课操作、打印课程信息（信息包括：编号、课程名称、上课地点、时间、授课教师 等）；模拟学生退课操作，再打印课程信息。
3.编写实验报告。

实验过程：
  1.编写实体类以及测试主类                         
  2.在测试主类中，实例化多个类实体，模拟学生选课操作、打印课程信息（信息包括：编号、课程名称、上课地点、时间、授课教师 等）；模拟学生退课操作，再打印课程信息。
核心代码：
  import xuanke.Teachers;
import xuanke.Students;
import java.util.Scanner;
public abstract class Test2 {

	public static void main(String[] args) {
		// People peo0= new People();每次定义为一个人，再分学生老师
		Students stu0 = new Students(1,"Lily","女","S1001",0);
		//Students stu1 = new Students("S1002","Bob");
		Teachers tea1 = new Teachers(1,"Sua","T1001","线性代数");
		Courses cou0 = new Courses(1,"线性代数","教104",0);
		
		for(;;) {
		System.out.println("<学生选课系统>");
		System.out.println("<学生信息>");
		System.out.println("编号   姓名   学号   课数");
		System.out.println("  "+stu0.getNo()+"  "+stu0.getStudentName()+" "+stu0.getStudentId()+"   "+stu0.getCourses());
		//System.out.println("Name:"+stu1.getStudentName()+"ID:"+stu1.getStudentId());
		Scanner reader = new Scanner(System.in);
		System.out.println("请输入学生编号：");
		int x =reader.nextInt();
		if(x==1) {//1号学生
			System.out.println("选课：请输入1");
			System.out.println("退课：请输入2");
			int y =reader.nextInt();
	        
		if(y==1){//1为选课
			System.out.println("<课程信息>");
			System.out.println("编号   课程名称   教学地点   选课人数");
			System.out.println("  "+cou0.getNo()+"      "+cou0.getName()+"     "+cou0.getAdd()+"           "+cou0.getStuNo());
			System.out.println("请输入选择课程编号：");
			int z =reader.nextInt();
			if(z==1) {
				cou0.addStuNo(cou0.getStuNo());
				stu0.addCourses(stu0.getCourses());
				System.out.println("选课人数"+cou0.getStuNo()+"选课数"+stu0.getCourses());
				System.out.println("<教师信息>");
				System.out.println("编号   姓名   学号   授课");
				System.out.println("  "+tea1.getNo()+"  "+tea1.getTeacherName()+" "+tea1.getTeacherId()+" "+tea1.getTeaCourse());
						}
			else {
				System.out.println("无此课程信息，请重新选择！");
			}
		}
		else if(y==2) {//2为退课
			System.out.println("<课程信息>");
			System.out.println("编号   课程名称   教学地点   选课人数");
			System.out.println("  "+cou0.getNo()+"      "+cou0.getName()+"     "+cou0.getAdd()+"           "+cou0.getStuNo());
			System.out.println("请输入选择课程编号：");
			int z =reader.nextInt();
			if(z==1) {
				cou0.reduceStuNo(cou0.getStuNo());
				stu0.reduceCourses(stu0.getCourses());
				System.out.println("选课人数"+cou0.getStuNo()+"选课数"+stu0.getCourses());
				System.out.println("<教师信息>");
				System.out.println("编号   姓名   学号   授课");
				System.out.println("  "+tea1.getNo()+"  "+tea1.getTeacherName()+" "+tea1.getTeacherId()+" "+tea1.getTeaCourse());
						}
			else {
				System.out.println("无此课程信息，请重新选择！");
			}
		}
		else System.out.println("输入有误，请输入1~2");
	}
		else System.out.println("没有相关学生信息");
	}
	}
实验结果：
  <学生选课系统>
<学生信息>
编号   姓名   学号   课数
  1  Lily S1001   0
请输入学生编号：
2
没有相关学生信息
<学生选课系统>
<学生信息>
编号   姓名   学号   课数
  1  Lily S1001   0
请输入学生编号：
1
选课：请输入1
退课：请输入2
2
<课程信息>
编号   课程名称   教学地点   选课人数
  1      线性代数     教104           0
请输入选择课程编号：
1
选课人数-1选课数-1
<教师信息>
编号   姓名   学号   授课
  1  Sua T1001 线性代数
实验感想： 我觉得这一次的实验难度很大，接受了很多帮助，希望以后能够有所进步。
