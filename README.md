# PythonKiss
# Python 1
import math

def main(I):

   i = set(I)

   x = set()

   for m in i:

       if (m<86 and m>-42):

           x.add(math.floor(m/8)+4*m)

   t = x.union(i)

   f = set()

   for l in x:

       if (l < -6 or l > 93 ):

           f.add(6*l)

   return len(t) - sum(f)



print(main({32, 64, -53, 43, -99, -12, -9, -72, 59, -67}))

print(main({-96, 1, -61, 69, 47, 17, -78, -41, 28, -33}))

# Python 2
def transcode(hex_string):

   

   num = int(hex_string, 16)

   

   

   X1 = (num >> 0) & 0b111        

   X2 = (num >> 3) & 0b111        

   X3 = (num >> 6) & 0b11111      

   X5 = (num >> 13) & 0b1111111    

   X6 = (num >> 20) & 0b1        

   

   result = (X5 << 14) | (X2 << 11) | (X1 << 6) | (X3 << 1) | X6

   

   

   return hex(result)



print(transcode('0x213ec'))  

print(transcode('0x1eebb3'))

print(transcode('0x146c4b'))

print(transcode('0xa25f1'))



