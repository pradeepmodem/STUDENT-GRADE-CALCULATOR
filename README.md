import java.util.Scanner;

public class Task2_StudentGradeCalculator {
    public static void main(String[] args) {
        Scanner in=new Scanner(System.in);
        System.out.println(" ________________________________");
        System.out.println("| Marks Range  |      Grade      |");
        System.out.println("|--------------|-----------------|");
        System.out.println("|     100      |        0        |");
        System.out.println("|    80-99     |        A        |");
        System.out.println("|    60-79     |        B        |");
        System.out.println("|    40-59     |        C        |");
        System.out.println("|     <39      |        F        |");
        System.out.println("|______________|_________________|");
        gradeCalculator(in);
    }
    static void gradeCalculator(Scanner input){

        System.out.print("Enter the number of subjects: ");

        int n=input.nextInt();
        int sum=0;

        for (int i = 0; i < n; i++) {
            System.out.print("Enter marks of subject "+(i+1)+" (out of 100): ");
            int marks=input.nextInt();
            sum+=marks;
        }

        float avg=(float)sum / n;

        System.out.println();
        System.out.println("Total marks obtained out of "+(n*100)+" : "+ sum);
        System.out.println("The average percentage: "+ avg+"%");

        if(avg==100){
            System.out.println("Grade obtained: O");
        }else if(avg<100 && avg>=80){
            System.out.println("Grade obtained: A");
        }
        else if(avg<80 && avg>=60){
            System.out.println("Grade obtained: B");
        }
        else if(avg<60 && avg>=40){
            System.out.println("Grade obtained: C");
        }
        else{
            System.out.println("Grade obtained: F");
        }
    }
}
