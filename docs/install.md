import math #for calculating square root

def grabList(): #function definition
ls = [] #initializing empty list
val = int(input("Enter the length of the list: ")) #taking user input and adding to list
for i in range(1, val+1):
print("Enter element",i,": ",end =" ")
x = int(input())
ls.append(int(x))
print("\nSample data: ",ls) #display list elements as per output screen
sd_calc(avg_calc,ls) #function call to calculate standard deviation

  
def avg_calc(ls): #function definition for calculating mean value
avg= int(sum(ls) / len(ls))
return avg


def sd_calc(avg_calc,ls): #function definition for calculating standard deviation
avg=avg_calc(ls)
val=len(ls)
ls2 = [] #initializing empty list 2
ls3= [] #initializing empty list3 for computing squared value
ls2.extend(ls) #copy list 1 elements to list 2
ls2[:] = [x - avg for x in ls2] #subtract avg from each list value
for i in ls2:
ls3.append(float(i**2))
avg2=float(sum(ls3) / len(ls3))
sd=float(math.sqrt(avg2)) #finding sq root
print("Standard Deviation: ",sd)
  
grabList()
