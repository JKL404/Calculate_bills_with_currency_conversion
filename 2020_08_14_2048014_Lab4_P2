#Program to demonstrate funtions in python
import sys,time,random
typing_speed = 50 #wpm for typing speed
#Function to type slow in console
def slow_type(t):
    for l in t:
        sys.stdout.write(l)
        sys.stdout.flush()
        time.sleep(random.random()*10.0/typing_speed)
    print('')
#slow_type function end//
items_des=['Qty','Price_$']
items_store={}
total_amt=0.0
cvrt_amt=0.0
tax=0.0
#function to store Items in items_store dictionary
def add_Items(*myitem):
  itm_Name=myitem[0]
  items_store[itm_Name]={}
  for item in items_des:
    items_store[itm_Name][item]=float(input(item+" : "))
  #using lambda function i am calculating total from the items i.e qty * price
  mytotal = lambda a, b : a * b
  items_store[itm_Name]["total"]=mytotal(items_store[itm_Name]["Qty"],items_store[itm_Name]["Price_$"])
  return float(items_store[itm_Name]["total"])
def USD():
  return total_amt
def AED():
  return round(total_amt*3.67,2)
def INR():
  return round(total_amt*74.85,2)
#print Starting message in console
print("\t WELCOME TO 2048014 WORLD NO 1 SHOPPING MALL\n\n")
customer_name=input("May I have your name? \n=> ")
#Calling my user_defined function 'slow_type' and passing strings into it
slow_type("\nGood Morning "+customer_name+", I am your Assistant.....\n I am here to help you!\n\n")
#Getting no of items they want to purchase
no_items=int(input("How many items do you have for checkout: "))
print("\nProvide Items details:")
for i in range(no_items):
  itm_Name=input("\nItem_"+str(i+1)+" Name : ")
  total_amt+=add_Items(itm_Name)
#Adding 5% tax in total_amt
total_amt=round(total_amt,2)
tax=round(total_amt*0.05,2)
total_amt+=tax
#Checking currency
print("\nWe only accept following Currencies:\n1.USD ($)\n2.AED (د.إ)\n3.INR (₹)\n")
currency=int(input("Input your currency type: "))
switcher={
  1: USD,
  2: AED,
  3: INR
}
func = switcher.get(currency, "INVALID CURRENCY!")
converter = lambda x : "$" if x ==1 else ("د.إ" if x == 2 else "₹")
print("\n\nYOUR TOTAL BILLS:")
print("*******************\n")
print("Sub_Total:",total_amt-tax)
print("tax",tax)
print("--------------------")
print("Total in USD",total_amt)
print("--------------------")
print("Total in",converter(currency),func())
print("____________________")


