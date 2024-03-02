# sumofnums
def sum_of_elements(numbers,exclude_negative=False):
    summary = 0  
    if  exclude_negative == False:
        for num in numbers:
            summary += num
    else:
        for num in numbers:
            if num >= 0:
                summary += num
    return summary
    
numbers = input("Enter a list of numbers: ")
numberslist = numbers.split()
for i in range(len(numberslist)):
    numberslist[i] = int(numberslist[i])

x = input("Do you want to exclude negative numbers? (YES/NO): ")
if x.upper() == "YES":
    exclude_negative = True
elif x.upper() == "NO":
    exclude_negative = False
else:
    print("ERROR!!!!!!!!!")

print(sum_of_elements(numberslist, exclude_negative))
