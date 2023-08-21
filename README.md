def calculate_flames(name1, name2):
    name1 = name1.lower().replace(" ", "")
    name2 = name2.lower().replace(" ", "")
    common_letters = set(name1) & set(name2)
    total_letters = len(name1) + len(name2) - 2 * len(common_letters)
    flames = ['Friends', 'Love', 'Affection', 'Marriage', 'Enemy', 'Sister']
    while len(flames) > 1:
        index = total_letters % len(flames) - 1
        flames.pop(index)
    return flames[0]
if __name__ == "__main__":
    name1 = input("Enter the first name: ")
    name2 = input("Enter the second name: ")
    relationship = calculate_flames(name1, name2)
    print("Relationship between", name1, "and", name2, "is:",relationship)

    
    
Output:
Enter the first name: mahesh
Enter the second name: namratha
Relationship between mahesh and namratha is: Friends

Process finished with exit code 0
