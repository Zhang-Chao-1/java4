# java4
一、实验目的：
1.掌握Java中抽象类和抽象方法的定义；
2.掌握Java中接口的定义，熟练掌握接口的定义形式以及接口的实现方法
3.了解异常的使用方法，并在程序中根据输入情况做异常处理
二、实验内容
  某学校为了给学生提供勤工俭学机会，也减轻授课教师的部分压力，准许博士研究生参与课程的助教工作。此时，该博士研究生有双重身份：学生和助教教师。
1.设计两个管理接口：学生管理接口和教师管理接口。学生接口必须包括缴纳学费、查学费的方法；教师接口包括发放薪水和查询薪水的方法。
2.设计博士研究生类，实现上述的两个接口，该博士研究生应具有姓名、性别、年龄、每学期学费、每月薪水等属性。
3.编写测试类，并实例化至少两名博士研究生，统计他们的年收入和学费。根据两者之差，算出每名博士研究生的年应纳税金额。
三、实验要求：
1.在博士研究生类”中实现各个接口定义的抽象方法;
2.对年学费和年收入进行统计，用收入减去学费，求得纳税额；
3.国家最新纳税标准（系数），属于某一时期的特定固定值，与实例化对象没有关系，考虑如何用static final修饰定义。
4.实例化研究生类时，可采用运行时通过main方法的参数args一次性赋值，也可采用Scanner类实现运行时交互式输入。
5.根据输入情况，要在程序中做异常处理。
四、实验流程:
1) 设计抽象类Student：
属性包括姓名（name）、学费（fee）；
2) 定义一个接口Salary：包含一个方法int getSalary();
3) 定义一个研究生类Graduate，继承Student类且实现Salary接口：
新增属性：收入（salary）
4) 定义一个教师类（Teacher）：
5) 定义一个大学类（University），通过void payOff（Salary s）方法给研究生和教师发放并打印工资
五、核心代码
下列代码展示了子类与父类之间的继承，以及抽象类接口的如何实现，以及完善函数单独功能。
ublic class Graduate extends Student implements Salary{
	public int salary;  
    
    public Graduate(String name) {  
        super(name);      
    }  
  
    @Override  
    public int getSalary() {  
        return 1500;  
    }  
  
    @Override  
    public void setFee(int fee) {  
          
    }  
  
    @Override  
    public int getFee() {  。
        return 0;  
    }  
      
    public boolean isLoan(){  
        if(getFee()<getSalary())    
            return false;     
        else                     
            return true;            
    }  
 
}`

六、实验感想
这次实验有点困难，在同学的帮助下还是完成了本次实验。
