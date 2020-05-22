# helloworld
package java8.features;

import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;
import java.util.logging.Level;
import java.util.logging.Logger;

public class SumOfSquareAndCubeLists {

	private static Logger logger=Logger.getLogger(Logger.GLOBAL_LOGGER_NAME);
	public static void main(String[] args) {
		//Declaring ListA & ListB
		List<Integer> listA=new ArrayList<>();
		List<Integer> listB=new ArrayList<>();
		//Declaring Scanner to read input data
		Scanner in = new Scanner(System.in);
		//Reading size of ListA
		logger.info("Enter No. of items in List A");
        int listASize = in.nextInt();
      //Reading size of ListB
        logger.info("Enter No. of items in List B");
        int listBSize = in.nextInt();
      //Reading Elements of ListA
        logger.info("Enter Elements of List A");
       for (int i=0;i<listASize;i++){
    	   listA.add(in.nextInt());
       }
       //Reading Elements of ListB
       logger.info("Enter Elements of List B");
       for (int i=0;i<listBSize;i++){
    	   listB.add(in.nextInt());
       }
       
       int sumSqr=listA.stream().mapToInt(l->l*l)
    		   					.sum();
       int sumCube=listB.stream().mapToInt(l->l*l*l)
    		   					 .sum();
       
       logger.info("Sum is: "+(sumSqr+sumCube));
	}

}
