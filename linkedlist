size = int(input('Enter the size of the list: '))
items = ['' for i in range (size)]
pointers = ['' for i in range (size)]
for count in range (size -1):
    pointers[count] = count + 1
pointers[size-1]= -1    
heapp=0
sp = -1
nullp = -1
oldindex = 0


def add():
    global sp,heapp,pointers,items
    if heapp == nullp :
        print('linkedlist is full, cannot add')
    else:
        itemadd = input('input the item to add: ')
        tempp =sp
        sp =heapp
        heapp = pointers[heapp]
        items[sp] = itemadd
        pointers[sp] = tempp
    print (items,pointers)    
    
    
def search():
        key= input('input an item to search: ')
        i= sp
        found = False
        while i !=  nullp and not found:
            if items[i] == key:
                print ('item found at location: ', i +1)
                break
            else:
                i = pointers[i]
        else:
            print('item not found')
    
            

def delete():
    global sp, heapp, items ,pointers, oldindex
    if sp == nullp:
        print ('list empty, cannot delete')
    else:
        itemdelete = input('enter the item to be deleted: ')
        index = sp
        while items[index] != itemdelete and index != nullp:
            oldindex = index
            index = pointers[index]
        if index == nullp:
            print('itemdelete not found')
        else:
            items[index]=''
            tempp = pointers[index]
            pointers[index] = heapp
            pointers[oldindex] = tempp
            heapp = index
        print(items,pointers)    



while True:
    menu = int(input('''please choose the option number
                  1. Insert
                  2. Delete
                  3. search
                  4. exit: '''))
    if menu == 1 :
        add()
    elif menu == 2:
        delete()
    if menu == 3 :
        search()
    elif menu == 4:
        break
    else:
        print ('chose an option between 1 - 4')
        
            
