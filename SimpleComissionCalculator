
package SimpleComissionCalculator;
// This allows for user input.
import java.util.Scanner;

//////////////////////////////////////////////////////////////////////////////////////ALLOWS ABILITY TO FORMAT DECIMALS
import java.text.DecimalFormat;
/**
 *
 * @author Frostysmooth aka Justin Mirabal
 */
public class SimpleComissionCalculator {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner input = new Scanner ( System.in );
        
        double salary = 40000; // base salary of salesperson
        double commissionRate = 0.08; // 8% commission on sales
        double accelerationRate = 1.2; // acceleration rate
        
        ///////////////////////////////////////////////////////////////////////////////////removed because they were not used in C.Drost's program
        //double minSales = 48000; // commission starts here, 80% of sales target
        //double salesTarget = 60000; // sales target
        
        String [] salesPerson;// Sales person's name
        salesPerson = new String[ 3 ];
        
        double [] salesAmt; // Sales person's amount
        salesAmt = new double[3];
        
        double [] totalComp; // Sales person's total compensation
        totalComp = new double[3];
                   
        
        DecimalFormat df = new DecimalFormat("#.00");//////////////////////////////////////////////ADDED ABILITY TO FORMAT DECIMALS
        
        //1st sales persons inputs name/sales
        System.out.print ("Enter the first salespersons name: ");
            salesPerson[0] = input.nextLine();
        System.out.print ("Enter the salespersons annual sales: $");
            salesAmt[0] = input.nextDouble();
            input.nextLine();
                  
        //2nd sales persons inputs name/sales
        System.out.print ("Enter the second salespersons name: ");
            salesPerson[1] = input.nextLine();
        System.out.print ("Enter the salespersons annual sales: $");
            salesAmt[1] = input.nextDouble();
            input.nextLine();
        
        //3rd sales persons inputs name/sales
        System.out.print ("Enter the third salespersons name: ");
            salesPerson[2] = input.nextLine();
        System.out.print ("Enter the salespersons annual sales: $");
            salesAmt[2] = input.nextDouble();
            input.nextLine();
        System.out.println();
            
//        for(int i=0; i<3; i++){              
//           if (salesAmt[i] < minSales) // sales less than $48,000
//                {  
//                  totalComp[i] = salary;
//                  //System.out.printf("The total compensation wil be %f%n", totalSalary);
//                  System.out.printf(df.format(salesPerson[i]) + "'s total compensation will be %f%n", totalComp[i]);
//                }
//           else if (salesAmt[i] < salesTarget) // sales between $48,001 - $60,000
//                {   
//                     totalComp[i] = salesAmt[i] * commissionRate + salary;
//                     System.out.printf ( df.format(salesPerson[i]) + "'s total compensation will be %f%n", totalComp[i]);
//                }
//            else if (salesAmt[i] >= salesTarget) // Sales over $60,000
//                {
//                     totalComp[i] = (salesAmt[i] * commissionRate * accelerationRate) + salary;
//                     System.out.printf ( df.format(salesPerson[i]) + "'s total compensation will be %f%n", totalComp[i]);
//                } // end else if
//        }  // end of for loop
//        
        
        
        ////////////////////////////////////////////////////////////////////////////////////ADDED FROM OTHER PROGRAM WITH SOME MODIFICATIONS
        /*
         * added new variables to match what was added
         */
        double Commission;
        double AnnualCompensation;
        double Bonus;
        //////////////////////////////////////////////////////////////////////////////////////kept for loop from J.Dudley's program
        /*
         * added sales comparison and calculations from C.Drost program with minor adjustments on the if/else if
         * to handle the for loop
         */
        for(int i=0; i<3; i++){ 
          if(salesAmt[i] >= 48000 && salesAmt[i] < 60000) // Runs if Annual Sales are over $48,000 otherwise is skipped.
            { // Starts the body of the if clause.
                Commission = (salesAmt[i] * commissionRate); // Sets the value of Commission to 8%.

            // Prints out the total amount of commission.
            System.out.println("\n" + "For " + salesPerson[i] + " The total commission is: $"
                              + Commission);
            
                 // Prints if 80% of target sales are met.
                System.out.println("Congratulations " + salesPerson[i] + "!" + " You reached 80% of target sales at "
                                  + "$48,000");
                
                // Sets Annual Compensation to total Salary & Commission only.
                AnnualCompensation = (Commission + salary);
                
                // Prints out the amount of Annual Compensation.
                System.out.println("The total annual compensation for " + salesPerson[i]
                                   + " is: $" + AnnualCompensation );
            }
               
               
            else if(salesAmt[i] >= 60000) // Nested if clause only runs if Annual Sales are over $60,000
            { // Starts the body of the nested if clause.                
                
                
                Commission = (salesAmt[i] * commissionRate); // Sets the value of Commission to 8%
                Bonus = (Commission * accelerationRate); // Sets the value of Bonus to 1.2%.
                
                // Prints out the total amount of commission.
                System.out.println("\n" + "For " + salesPerson[i] + " The total commission is: $"
                              + Commission);
                
                // Prints out the bonus amount with commission
                System.out.println("\n" + "For " + salesPerson[i] + " The total bonus with acceleration factor is: $"
                              + Bonus);
                
            
                // Prints out the total amount of the Bonus.
                System.out.println("\n Congratulations " + salesPerson[i] + "!" + " You reached the sales target of "
                                  + "$60,000");

                // Sets Annual Compensation to total of Salary, Commission, & Bonus all together.
                AnnualCompensation = (Bonus + salary);

                // Prints out the amount of Annual Compensation.
                System.out.println("The total annual compensation for " + salesPerson[i] 
                                   + " is: $" + AnnualCompensation );
            } // Ends the body of the nested if clause.

            else if (salesAmt[i] < 48000)

            { // Starts the body of the else clause


                // Prints that the Salesperson didn't reach 80% of the Sales Target
                System.out.println("\n" + "Aww, sorry " + salesPerson[i] + "." + " You didn't meet 80% of target sales "
                              + "and have not earned a commission or a bonus. ");

                // Sets the Annual Compensation to the amount of the Fixed Salary.
                AnnualCompensation = salary;

                // Prints the amount of Annual Compensation without the commission & bonus.
                System.out.println("The total annual compensation for " + salesPerson[i] + 
                                   " is: $" + AnnualCompensation );
            } // Ends the body of the else clause.
          }
        
        
        
        
        System.out.println();
        
        
        ///////////////////////////////////////////////////////////////////////////////NEEDED TO MODIFY 
        /*
         * changed z from -1 to 0 and 
         * then had to change any references from a to z
         * changing any reference from z to a
         */
        int z = 0;
        double max = totalComp[0];        
         for (int counter = 0; counter < totalComp.length; counter++)

           if (totalComp[counter] > max)
           {
           max = totalComp[counter];
           z = counter;
           }

          for (int a = 0; a < 3; a++)
          {
               if (a==z)
               {
                    System.out.println("The highest sales belongs to " + salesPerson[z]);
               }
               else
               {
                    double test1 = salesAmt[z];
                    double test2 = salesAmt[a];
                    double Diff = test2 - test1;
                    System.out.println(salesPerson[z] + " needed to sell " + df.format(Diff) + " more dollars");
               }

          }
        

    }
}
