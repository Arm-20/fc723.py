class GCDAlgorithm:
"""
this class implements the GCDAlgorithm to find the greatest common divisor (GCD).
"""
    
    def compute_gcd(A, B):
        """
        This method calculates the GCD of two positive integers using the Euclidean Algorithm.
        """
        while B != 0:  # Continue until the remainder becomes 0
            prev = B   # Store the current value of B
            B = A % B  # Remainder
            A = prev   # Update 'A' to be the previous value of 'B'
        return A

def get_user_input():
     """
     this function accepts input and calculates the GCD.
     """
     try:
          A = int(input("please enter the firts positve integer: "))
          B = int(input("please enter the second positive integer: "))
          # Input validation
          if A <= 0 or B <= 0:
              print("Error: Both numbers must be positive integers.")
              return None
          return (A, B)
    except ValueError:
        print("Error: Please enter valid integers.")
        return None
# Main
data = get_user_input()
if data:
    gcd = GCDAlgorithm.compute_gcd(data[0], data[1])    # 
    print(f"The GCD of {data[0]} and {data[1]} is: {gcd}")
