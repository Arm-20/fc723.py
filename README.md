class GCDAlgorithm:
"""
this class implements the GCDAlgorithm to find the greatest common divisor (GCD).
"""
@staticmethod
def compute_gcd(A, B):
  """
  this method calculates the GCD of two positive integers the Euclidean Algorithm.
  """
  while B !=0:  #continue until the remainder becomes 0
      prev = B  #store the current value of B
      B = A % B #remainder
      A = prev  #Update 'A' to be the previous value of 'B'
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
