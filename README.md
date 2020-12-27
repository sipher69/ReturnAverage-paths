# ReturnAverage-paths
up to the user input the output will be the path crossed based on the user input 
/*
*************************************************************
*              Student Name: SAIF NITHAM AL-JELANI          *
*              University ID :3170605191                    *
*              Subject : Software testing project           *
*************************************************************
*/
 

package pkg3170605191;
import java.util.Scanner;
/**
 *
 * @author sipher
 */
public class S_3170605191 {

    /**
     * @param args the command line arguments
     */
    public static double ReturnAverage(int value[],  int AS, int MIN, int MAX,int o){
    

         int i, ti, tv, sum; double av = 0; //Define variables

         
          //"First step we I defined the variables 
         i = 0; ti = 4; tv =0; sum = 0;//Give variables values
         
         if(o==0){
         System.err.print("1-2-");

          //Second step I gave each  variable a Value AS>ti && value[i] == -999) {System.err.println("3(T)-4(F)-10");
          if(AS>ti && value[i] == -999) {System.err.print("3(T)-4(F)-");}
          else if (AS>ti && value[i] != -999) {System.err.print("3(T)-4(T)-5-");}
          else{System.err.print("3(T)-");}

          
          //if(value[i] != -999){System.err.println("4(T)-5");}
         // else{System.err.println("4(F)-10");}
         while (ti < AS && value[i] != -999) /*While loop*/
         {
            ti++;
        
            if (value[i] >= MIN && value[i] <= MAX)/*if statment for node number 6 and 7*/ {
               tv++; //Counter increments # 1 for tv variable
             System.err.print("6(T)-7(T)-8-");
               sum = sum + value[i]; //giving the sum new value after summing the sum and the index[i] on the array
            }
            System.err.print("9-");
            i++; //Counter increments # 1 for i variable
            if(AS>ti){System.err.print("3(T)-");}
            else {System.err.print("3(F)-");}
            
         }
//         
          
         if (tv > 0) /*if statment node number 10*/
         {
             System.err.print("10(T)-12-13");
            av = (double)sum/tv;//giving the av new value after dividing the sum on av
                         

         }
        // else 
             //if(tv<0){System.err.print("10(F)-11-13");}
         else{
             System.err.print("10(F)-11-13");
            av = (double) -999;
            
         }
           return (av);
          //return the variable av
         }
         else{
              
         if(ti>AS){
             if(value[i]!=-999){
              System.err.print("1-2-3-7-");
        
         }} else
         
         if(value[i]!=-999){
             if(ti<AS){System.err.print("4-");ti++;}
             
                     if(value[i]>=MIN&&value[i]<=MAX){
                            System.err.print("5-6-3-");tv++;sum=sum+value[i];
                                           i++;}
         
         else
         {
             System.err.print("4-6-3-");
         i++;
         }}
             
             
         if(tv>0){System.err.print("9-10");av=(double)sum/tv;}
         else{System.err.print("8-10");av=(double)-999;}
         
         
         }
                    return (av);

    }
       
    
    
    
    public static void main(String[] args) {
        // main method
        Scanner sc=new Scanner(System.in);
        
        int value[] = new int[50];
        int r = 0;
         System.out.println("Insert 0 for Control Flow Testing or 1 for Data Flow Testing  ");
         
        int o = sc.nextInt();
        System.out.println("please enter the size of the array");
       int AS=sc.nextInt();
       System.out.println("please insert element to your array ");
               

       for(int i=0;i<=AS;){
       value[r] = sc.nextInt();
       i++;
       }
       System.out.println("please enter the MIN number  ");
      int MIN= sc.nextInt();
       System.out.println("please enter the MAX number  ");
        int MAX= sc.nextInt();
        

        
       ReturnAverage(value, AS, MIN, MAX,o);
      //call the ReturnAverage method
    
     }
    
}
