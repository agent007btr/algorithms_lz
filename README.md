import random
numbers = []
while len(numbers) < 100:
    numbers.append(random.randint(0, 1000000))
print("исходный список", numbers)
def bubble_sort(nums):
    a = True
    b = 1
    while a:
        a = False
        for i in range(len(nums) - 1):  
            if nums[i] < nums[i + 1]:  
                nums[i], nums[i + 1] = nums[i + 1], nums[i]
                a = True
        print( "после пузырька" , nums)
bubble_sort(numbers)
def selection_sort(nums):
    for i in range(len(nums)):
        lowest_value_index = i
        for j in range(i + 1, len(nums)):
            if nums[j] > nums[lowest_value_index]: 
                lowest_value_index = j
        nums[i], nums[lowest_value_index] = nums[lowest_value_index], nums[i]
        print("после выборки", nums)
selection_sorted = selection_sort(numbers)
# algorithms_lz
