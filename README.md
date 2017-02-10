/*Andrew Opio
 * ArrayList practice
 */
import java.util.*;
public class Arraylists {
	public static void main(String[] args) {
	    // TODO Auto-generated method stub
	    ArrayList<String> letterList = new ArrayList<String>();
	    letterList.add("A");
	    letterList.add("B");
	    letterList.add("C");
	    letterList.add("D");
	    letterList.add("E");
	    letterList.add("F");
	    letterList.add("G");
	    letterList.add("H");
	    //method1(letterList);
	    //method2(letterList);
	    //method3(letterList);
	    //method4(letterList);
	    //method5(letterList);
	    //method6(letterList);
	    method7(letterList);


	}
	public static void method1(ArrayList<String> letterList){
	    for(int i=0; i<letterList.size(); i++){
	        if(i ==0)
	        if(letterList.get(i).equals("A"))
	            letterList.add(i, "A");
	        else
	            if(letterList.get(i+1).equals("A"))
	                letterList.add(i, "A");
	    }



	    for(int i=0; i<letterList.size(); i++)
	        System.out.print(" " +letterList.get(i));

	}

	public static void method2(ArrayList<String> letterList){
	        for(int i=0; i<letterList.size(); i++){



	                if(letterList.get(i).equals("B")){
	                letterList.remove(i);
	                letterList.add(i, "z");
	            }
	        }

	        

	}
	public static void method3(ArrayList<String> letterList){
	    for(int i=0; i<letterList.size(); i++){
	        if(letterList.get(i).equals("C")){
	            letterList.remove(i);
	            }
	        }
	  
	    }
	public static void method4(ArrayList<String> letterList){
	    Random rand = new Random();
	    int num = rand.nextInt(letterList.size());


	    for(int i =0; i<letterList.size();i++){
	        if(letterList.get(i)=="D"){

	            while(num ==i){
	             num = rand.nextInt(letterList.size());
	            }


	            }

	        }
	    letterList.set(num, "D");
	

	        }

	public static void method5(ArrayList<String> letterList){
	    Random rand = new Random();
	    int num = rand.nextInt(letterList.size());
	    int index =0;
	    for(int i =0; i<letterList.size();i++){
	        if(letterList.get(i)=="E")
	            index = i;
	    }
	    while(num == index)
	        num = rand.nextInt(letterList.size());
	    letterList.remove(index);
	    letterList.add(num, "E");

	


	}
	public static void method6(ArrayList<String> letterList){
	    Random rand = new Random();
	    int letter = rand.nextInt(letterList.size());
	    int num = rand.nextInt(letterList.size());
	    int index =0;
	    for(int i =0; i<letterList.size();i++){
	        if(letterList.get(i)=="F")
	            index = i;
	    }
	    String str = letterList.get(num);
	    letterList.set(num,letterList.get(letter));
	    letterList.set(letterList.indexOf(letterList.get(letter)), str);

	   

	}
  public static void method7(ArrayList<String> letterList){
	  Random rand = new Random();
	    int letter = rand.nextInt(letterList.size());
	    
	    for(int i =0; i<letterList.size();i++)
	        if(letterList.get(i)=="G"){
	        	while(letter == i){
	        		letter = rand.nextInt(letterList.size());
	        	}
	        	letterList.set(i,letterList.get(letter) );
	        }
	    for(int i =0; i<letterList.size();i++)
	        System.out.print(" "+letterList.get(i));
  }

}
