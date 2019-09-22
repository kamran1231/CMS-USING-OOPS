# CMS-USING-OOPS


#CUSTOMER MANAGEMENT SYSTEM USING OOPS

class Customer :   #class
    list_cus = []
    #constructon
    def __init__(self):
        self.id = 0
        self.name = 0
        self.age = 0
        self.address = 0
        self.city = 0


    #fuction/method for add a customer
    def add_cus(self):
        Customer.list_cus.append(self)

    #function/method for search customer by id.
    def search_cus(self):
        for i in Customer.list_cus:
            if (i.id == self.id):
                print('cusID:',i.id,'cusName:',i.name,'cusAge:',i.age,'cusAddress:',i.address,'cusCity:',i.city)

    #function/method for search customer by name.
    def search_cus_name(self):
        for i in Customer.list_cus:
            if (i.name == self.name):
                print('cusID:', i.id, 'cusName:', i.name, 'cusAge:', i.age, 'cusAddress:', i.address, 'cusCity:',
                      i.city)

    #function/method for Delete the customer by id.
    def delete_cus(self):
        for i in Customer.list_cus:
            if (i.id == self.id):
                Customer.list_cus.remove(i)
                print('customer details Deleted Successfully.')

    #function/method for Delete the customer by name.
    def delete_cus_name(self):
        for i in Customer.list_cus:
            if (i.name == self.name):
                Customer.list_cus.remove(i)
                print('customer details Deleted successfully.')


    #function/method for Modify the customer by Id.
    def modify_cus(self):
        for i in Customer.list_cus:
            if (i.id == self.id):
                i.name = self.name
                i.age = self.age
                i.address = self.address
                i.city = self.city

    #function/method for Modify the customer by Name.
    def modify_cus_name(self):
        for i in Customer.list_cus:
            if (i.name == self.name):
                i.id = self.id
                i.age = self.age
                i.address = self.address
                i.city = self.city

    #function/method for display all customer details.
    def display_all_cus(self):
        for i in Customer.list_cus:
            print('cusID:', i.id, 'cusName:', i.name, 'cusAge:', i.age, 'cusAddress:', i.address, 'cusCity:',
                  i.city)









#PL
while True:
    print('WELCOME TO MY CUSTOMER MANAGEMENT SYSTEM')
    print('1. ADD CUSTOMER \n 2. SEARCH CUSTOMER \n 3. DELETE CUSTOMER \n '
          '4. MODIFY CUSTOMER \n 5. DISPLAY ALL CUSTOMER')
    choice = input('enter the user choice: ')
    if choice == '1':   #Add customer
        print('you choosed "ADD CUSTOMER" so please fill the all entry for add customer')
        cus = Customer()
        cus.id = int(input('enter the customer id: '))
        cus.name = input('enter the customer name: ')
        cus.age = int(input('enter the customer age: '))
        cus.address = input('enter the customer address: ')
        cus.city = input('enter the customer city: ')
        cus.add_cus()
        print('Details of all customer is added successfully.')

    elif choice == '2':
        cus = Customer()
        print('you chosed "SEARCH CUSTOMER"')
        print('1. SEARCH BY ID.  \n 2. SEARCH BY NAME.')
        choice = input('enter you choice for search the customer:')
        if choice == '1':
            print('you chosed "SEARCH BY ID:"')
            cus.id = int(input('enter the customer id for search the customer Details: '))
            cus.search_cus()
        elif choice == '2':
            print('you chosed "SEARCH BY NAME:"')
            cus.name = input('enter the customer name for search the customer Details: ')
            cus.search_cus_name()

    elif choice == '3':
        cus = Customer()
        print('you chosed "DELETE CUSTOMER"')
        print('1. DELETE CUSTOMET BY ID: \n 2. DELETE CUSTOMER BY NAME:')
        choice = input('enter the choice: ')
        if choice == '1':
            print('you chosed "DELETE BY ID:"')
            cus.id = int(input('enter the customer id for Delete the customer: '))
            cus.delete_cus()

        elif choice == '2':
            print('you chosed "DELETE BY NAME:"')
            cus.name = input('enter the customer name for Delete the customer: ')
            cus.search_cus_name()

    elif choice == '4':
        cus = Customer()
        print('you chosed "MODIFY CUSTOMER:"')
        print('1. MODIFY BY ID: \n 2. MODIFY BY NAME:')
        choice = input('enter your choice: ')
        if choice == '1':
            print('you chosed Modify by Id:')
            cus.id = int(input('enter the customer id for modify the details of customer: '))
            cus.name = input('enter the customer update name: ')
            cus.age = int(input('enter the customer update age: '))
            cus.address = input('enter the customer update address: ')
            cus.city = input('enter the customer update city: ')
            cus.modify_cus()
            print('customer details is updated successfully.')

        elif choice == '2':
            print('you chosed Modify by Name:')

            cus.name = input('enter the customer name for modify the customer details : ')
            cus.id = int(input('enter the customer update id : '))

            cus.age = int(input('enter the customer update age: '))
            cus.address = input('enter the customer update address: ')
            cus.city = input('enter the customer update city: ')
            cus.modify_cus_name()
            print('customer details is updated successfully.')

    elif choice == '5':
        cus = Customer()
        # print('you chosed Display all customer details:')
        # for i in Customer.list_cus:
        #     print('cusID:', i.id, 'cusName:', i.name, 'cusAge:', i.age, 'cusAddress:', i.address, 'cusCity:',
        #           i.city)

        cus.display_all_cus()






