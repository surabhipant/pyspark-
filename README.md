# pyspark-
# # import re
# #
# # str1 = "D:\LandingArea\Finet\\Kiribati\KI.CV756GL1.20220608.DW"
# # p = re.compile(r"[_\.](\d+)\.")
# # print(p.sub(r'yyyymmdd', str1))
# # print(p.search(str1).groups()[-1])
# # print(str1.replace(p.search(str1).groups()[-1], "yyyymmdd"))
#
#
#
#
# def reverse_str(inputstring):
#
#     rev_str = inputstring[::-1]
#
#
#     return(rev_str)
#
#
# inputstring ='any'
# print(" the original string is " + inputstring)
# #
# print(" teh rev string is " + reverse_str(inputstring))
#
#
# # def reverse_str(s):
# #     str = ""
# #     for i in s:
# #         print(i)
# #         str = i + str
# #
# #     return str
# #
# #
# # print(reverse_str('any'))
#
#
# # def anagrams(str1, str2):
# #
# #     if len(str1) != len(str2):
# #         return False
# #
# #     count = {}
# #
# #     for i in str1:
# #         if i in count:
# #             count[i] = count[i] + 1
# #         else:
# #             count[i] = 1
# #
# #
# #     for i in str2:
# #         if i in count:
# #             count[i] = count[i] - 1
# #         else:
# #             count[i] = 1
# #
# #     print(count)
# #
# #     for i in count:
# #         if count[i] != 0:
# #             return False
# #
# #     return True
# #
# #
# #
# # print(anagrams('god','dog'))



# def pair_sum(arr,k):
#     if len(arr) < k :
#         return False
#
#     seen = set()
#     output = set()
#
#     for i in arr:
#         target = k - i
#         if target not in seen:
#             seen.add(i)
#         else:
#             output.add((min(i,target),max(i,target)))
#
#     return (print(output))
#
# print(pair_sum([1,3,2,2], 4))


# def finder(arr1,arr2):
#     cnt_aar1 ={}
#     cnt_aar2 = {}
#
#
#     for i in arr1:
#         if i in cnt_aar1:
#             cnt_aar1[i] = cnt_aar1[i] + 1
#         else:
#             cnt_aar1[i] = 1
#
#     print(cnt_aar1)
#
#     for i in arr2:
#         if i in cnt_aar2:
#             cnt_aar2[i] = cnt_aar2[i] + 1
#         else:
#             cnt_aar2[i] = 1
#
#     print(cnt_aar2)
#
#     for i in cnt_aar1:
#         if i not in cnt_aar2:
#             print (" the missing number is " + str(i))
#
# finder([1,2,3,4],[4,2,3])



# arr=[1,2,-1,3,4,10,10,-10,-1]
#
# def cnt_sum(arr):
#     curr_sum = arr[0]
#     max_sum = arr[0]
#
#     for i in arr[1:]:
#         curr_sum = max(curr_sum+i,i)
#         max_sum = max(curr_sum, max_sum)
#
#     print(max_sum)
#
#
# cnt_sum(arr)


# str1 = "the quick brown fox"
# str2 =""
# emp =[]
#
# #print(len(str1))
#
# # splitted = str1.split()
# # print(splitted)
# #
# # for i in splitted:
# #     str2 = i + ' ' +  str2
#
#
# for i in str1:
#   str2 = i + str2
#
# print(str2)






# input_str ='AAABBC'
#
# def compression (input_str):
#
#     cnt = 0
#     final_str =''
#     t = len(input_str)
#     print(t)
#
#     for i in range(len(input_str)-1):
#         ##print(i)
#
#         if input_str[i+1] == input_str[i]:
#             cnt = cnt + 1
#             a = input_str[i]
#             print(a)
#             if i == t - 2:
#                 a = input_str[i + 1]
#                 cnt = cnt + 1
#                 final_str = final_str + a + str(cnt)
#
#
#
#         else:
#
#
#             cnt = cnt + 1
#             #a = input_str[i + 1]
#             final_str = final_str + a + str(cnt)
#             print(final_str)
#             cnt = 0
#
#         if (input_str[i+1] != input_str[i]):
#             if (i == t - 2):
#                 a = input_str[i + 1]
#                 cnt = cnt + 1
#                 final_str = final_str + a + str(cnt)
#
#
#
#     return final_str
#
# print(compression(input_str))


# class Userdefinition:
#     def __init__(self,name,age):
#         self.name = name
#         self.age = age
#         print(f"hello my name is {self.name}and my age is {self.age}")
#
#
# class Archer(Userdefinition):
#     def calculate(self,x,y):
#         return(x+y)
#
#
#
# a1 = Archer('surabhi',31)
# print(a1.calculate(10,20))



# def fibo():
#     a = 0
#     b = 1
#
#     for i in range(4):
#         yield b
#         a , b = b, a+b
#
#
# alpha = fibo()
# print(next(alpha))
# print(next(alpha))
# print(next(alpha))
# print(next(alpha))
# print(next(alpha))


# from functools import reduce
#
# a = [1,2,3,4]
#
# ans = reduce(lambda x,y: x+y, a)
# print(ans)

[0,1,1,2,3,5]

# def genfibbo(n):
#
#     a =[]
#
#     for i in range(n):
#         if i == 0:
#             a.append(0)
#         if i == 1:
#             a.append(1)
#         if i > 1:
#             a.append(a[i-1] +a[i-2])
#     return(a)
#
#
# print(genfibbo(6))






## this is not a balnced string  [{()}]

def balanced_str(s):
    a = set('[{(')

    stack = []

    matching = set((('[',']'),('{','}'),('(',')')))

    if len(s) == 0:
        return True

    for i in s:
        if i in a:
            stack.append(i)

        else:

            if len(stack) == 0:
                return False

            last_lement = stack.pop()

            if (last_lement,i) in matching:
                return True


print(balanced_str('[{(})}]'))


minimum discount problem:

# Online Python compiler (interpreter) to run Python online.
# Write Python 3 code in this online editor and run it.
prices = [4,9,2,3]

def compute(prices):
    
    a =[]
    sum = 0
    
    for i in range(len(prices)):
        if i == 0:
            a.append(0)
        else :
           t = max(prices[i]-prices[i-1],0)
           a.append(t)
           sum = sum + t
    sum = sum + prices[0]
    return(sum)
    
    
    
print(compute(prices))


###########implement a doublly linked list##########
The code is as follows:
comitted in 20th Apr,2023.
####################################################
 def __init__(self,value):
        self.value = value 
        self.next_value = None 
        self.prev_value = None
        


a = Node(1)
b = Node(2)
c = Node(3)

a.next_value = b
b.prev_value = a
b.next_value = c
c.prev_value = b

print(a.value)
print(a.next_value.value)
print(b.next_value.value)
print(b.prev_value.value)
        
    
    




























