# Find-algorithm
import csv
with open('/home/user/Downloads/P1_data.csv', 'r') as f: 
    reader = csv.reader(f) 
    headers = next(reader) 
    your_list = list(reader) 
h = [['0', '0', '0', '0', '0', '0']] 
for i in your_list: 
    print(i)
    if i[-1] == "TRUE":
        j = 0
        for x in i:
            if x != "TRUE":
                if x != h[0][j] and h[0][j] == '0':
                    h[0][j] = x 
                elif x != h[0][j] and h[0][j] != '0': 
                    h[0][j] = '?' 
                else: 
                    pass 
            j = j + 1

print("The maximally specific hypothesis for a given training example is: ") 
print(h)

Data set
Sunny	Warm	Normal	Strong	Warm	Same	Yes
Sunny	Warm	High	Strong	Warm	Same	Yes
Rainy	Cold	High	Strong	Warm	Change	No
Sunny	Warm	High	Strong	Cool	Change	Yes

Output

unfile('/home/user/.config/spyder-py3/temp.py', wdir='/home/user/.config/spyder-py3')
['Sunny', 'Warm', 'High', 'Strong', 'Warm', 'Same', 'Yes']
['Rainy', 'Cold', 'High', 'Strong', 'Warm', 'Change', 'No']
['Sunny', 'Warm', 'High', 'Strong', 'Cool', 'Change', 'Yes']
The maximally specific hypothesis for a given training example is: 
[['0', '0', '0', '0', '0', '0']]
