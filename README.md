# Task-Scheduler
import numpy as np
from datetime import date
def number_of_days(date_1,date_2):
    return (date_2 - date_1).days
def view_tasks(sorted_dict1,sorted_dict2):
    task=list(sorted_dict1.keys())
    deadline=list(sorted_dict2.keys())
    duration=list(sorted_dict1.values())
    print()
    for i in range(len(task)):
        print("TASK:",task[i])
        print("DEADLINE:",deadline[i])
        print("DURATION TO COMPLETE THE TASK:",duration[i])
        print()
dict1={}
dict2={}
print("TASK SCHEDULER")
print("enter category")
print("1.)WORK \n2.)HOME \n3.)PERSONAL\n")
space=int(input())
if space== 1:
    print("WORK:\n")
    while(1):
        task=input("enter your task:")
        a=list(map(int,input("Enter the deadline in yyyy mm dd format : ").strip().split()))[:3]
        for i in range(len(a)):
            yy=a[i]
            mm=a[i+1]
            dt=a[i+2]
            break
        date_2=date(yy,mm,dt)
        date_1=date.today()
        duration=number_of_days(date_1,date_2)
        dict1[task]=duration
        dict2[date_2]=duration
        ans=input("\ndo you want to add more tasks? y/n")
        if ans=='n':
            break
    keys = list(dict1.keys())
    values = list(dict1.values())
    sorted_value_index = np.argsort(values)
    sorted_dict1= {keys[i]: values[i] for i in sorted_value_index}
    keys2 = list(dict2.keys())
    values2 = list(dict2.values())
    sorted_value_index2 = np.argsort(values2)
    sorted_dict2= {keys2[i]: values2[i] for i in sorted_value_index2}
    view_tasks(sorted_dict1,sorted_dict2)

if space== 2:
    print("HOME:\n")
    while(1):
        task=input("enter your task:")
        a=list(map(int,input("Enter the deadline in yyyy mm dd format : ").strip().split()))[:3]
        for i in range(len(a)):
            yy=a[i]
            mm=a[i+1]
            dt=a[i+2]
            break
        date_2=date(yy,mm,dt)
        date_1=date.today()
        duration=number_of_days(date_1,date_2)
        dict1[task]=duration
        dict2[date_2]=duration
        ans=input("\ndo you want to add more tasks? y/n")
        if ans=='n':
            break
    keys = list(dict1.keys())
    values = list(dict1.values())
    sorted_value_index = np.argsort(values)
    sorted_dict1= {keys[i]: values[i] for i in sorted_value_index}
    keys2 = list(dict2.keys())
    values2 = list(dict2.values())
    sorted_value_index2 = np.argsort(values2)
    sorted_dict2= {keys2[i]: values2[i] for i in sorted_value_index2}
    view_tasks(sorted_dict1,sorted_dict2)

if space== 3:
    print("PERSONAL:\n")
    while(1):
        task=input("enter your task:")
        a=list(map(int,input("Enter the deadline in yyyy mm dd format : ").strip().split()))[:3]
        for i in range(len(a)):
            yy=a[i]
            mm=a[i+1]
            dt=a[i+2]
            break
        date_2=date(yy,mm,dt)
        date_1=date.today()
        duration=number_of_days(date_1,date_2)
        dict1[task]=duration
        dict2[date_2]=duration
        ans=input("\ndo you want to add more tasks? y/n")
        if ans=='n':
            break
    keys = list(dict1.keys())
    values = list(dict1.values())
    sorted_value_index = np.argsort(values)
    sorted_dict1= {keys[i]: values[i] for i in sorted_value_index}
    keys2 = list(dict2.keys())
    values2 = list(dict2.values())
    sorted_value_index2 = np.argsort(values2)
    sorted_dict2= {keys2[i]: values2[i] for i in sorted_value_index2}
    view_tasks(sorted_dict1,sorted_dict2)
