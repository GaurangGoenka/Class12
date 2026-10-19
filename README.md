import java. util.Scanner;
public class Adder
{
    int a[]=new int[2];
    Scanner sc=new Scanner( System.in);
    Adder()
    {
        a[0]=0;
        a[1]=0;
    }

    void readtime()
    {
        System.out.println("Enter hours and minutes");
        Scanner sc = new Scanner(System.in);
        a[0]=sc. nextInt();
        a[1]=sc. nextInt();
    }

    void disptime()
    {
        System. out.println("Hours=" + a[0]);
        System.out.println("Minutes="  + a[ 1]);
    }

    void addtime(Adder X,Adder Y)
    {
        a[1]=X.a[1] + Y.a[1];
        if(a[1]>=60)
        {
            a[0]=a[1]/60;
            a[1]=a[1]%60;
        }
        a[0] += X.a[0] + Y.a[0];
    }

    public static void main()
    {
        Adder ob1=new Adder();
        Adder ob2=new Adder();
        Adder ob3=new Adder();
        ob1.readtime();
        ob2.readtime() ;
        ob3.addtime(ob1,ob2);
        ob3.disptime();
    }

}
