// ToDo 01:

public class Main {
  public static void main(String[] args) {
    // Variable to store the current triangle number
    int triangleNumber = 0;
    int divisorsCounter = 0;
    int counter = 1;
    
    // Loop until a triangle number with over 100 divisors is found
    while (divisorsCounter <= 100) {  
      triangleNumber = triangleNumber + counter;
      divisorsCounter = 0;
      // Iterate from 1 up to the square root of the triangle number to find divisors
      for (int i = 1; i * i <= triangleNumber; i++) { 
        if (triangleNumber % i == 0) {
          // Increment the divisor counter by 2
          divisorsCounter += 2; // Considering both divisors: i and triangleNumber / i
          if (i * i == triangleNumber) {
            divisorsCounter--;
          }
        }
      }
	  
      counter++;
    }
    
    System.out.println("The first triangle number with over one hundred divisors is " + triangleNumber);
  }
}

// Todo 02: The value is 73920
