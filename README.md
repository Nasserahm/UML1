# Class for handling reservation details
class Reservation:
    # Constructor for initializing reservation attributes
    def __init__(self, reservation_id="", name="None", email="", hotel_name="", check_in="", check_out=""):
        self.reservation_id = reservation_id
        self.name = name
        self.email = email
        self.hotel_name = hotel_name
        self.check_in = check_in
        self.check_out = check_out

    # Setter method for reservation ID
    def setReservationID(self, reservation_id):
        self.reservation_id = reservation_id

    # Getter method for reservation ID
    def getReservationID(self):
        return self.reservation_id

    # Setter method for name
    def setName(self, name):
        self.name = name

    # Getter method for name
    def getName(self):
        return self.name

    # Setter method for email
    def setEmail(self, email):
        self.email = email

    # Getter method for email
    def getEmail(self):
        return self.email

    # Setter method for hotel name
    def setHotelName(self, hotel_name):
        self.hotel_name = hotel_name

    # Getter method for hotel name
    def getHotelName(self):
        return self.hotel_name

    # Setter method for check-in date
    def setCheckIn(self, check_in):
        self.check_in = check_in

    # Getter method for check-in date
    def getCheckIn(self):
        return self.check_in

    # Setter method for check-out date
    def setCheckOut(self, check_out):
        self.check_out = check_out

    # Getter method for check-out date
    def getCheckOut(self):
        return self.check_out

    # Method to generate a reservation receipt
    def generate_receipt(self):
        print("Generating receipt for", self.getName())

    # Method to cancel the reservation
    def cancel_reservation(self):
        print(f"Reservation {self.getReservationID()} has been cancelled")


# Class for handling room details
class Room:
    # Constructor for initializing room attributes
    def __init__(self, room_type="", number_of_rooms=1, nights=1, room_cost=0.0):
        self.room_type = room_type
        self.number_of_rooms = number_of_rooms
        self.nights = nights
        self.room_cost = room_cost
        self.total_charges = 0.0

    # Setter method for room type
    def setRoomType(self, room_type):
        self.room_type = room_type

    # Getter method for room type
    def getRoomType(self):
        return self.room_type

    # Setter method for number of rooms
    def setNumberOfRooms(self, number_of_rooms):
        self.number_of_rooms = number_of_rooms

    # Getter method for number of rooms
    def getNumberOfRooms(self):
        return self.number_of_rooms

    # Setter method for number of nights
    def setNights(self, nights):
        self.nights = nights

    # Getter method for number of nights
    def getNights(self):
        return self.nights

    # Setter method for room cost per night
    def setRoomCost(self, room_cost):
        self.room_cost = room_cost

    # Getter method for room cost per night
    def getRoomCost(self):
        return self.room_cost

    # Method to calculate the total charges for the room
    def calculate_total_charges(self):
        self.total_charges = self.room_cost * self.number_of_rooms * self.nights
        return self.total_charges


# Class for handling customer details
class Customer:
    # Constructor for initializing customer attributes
    def __init__(self, name="None", gender="", email="", phone_number="", billing_name="", credit_card_info=""):
        self.name = name
        self.gender = gender
        self.email = email
        self.phone_number = phone_number
        self.billing_name = billing_name
        self.credit_card_info = credit_card_info

    # Setter method for customer name
    def setName(self, name):
        self.name = name

    # Getter method for customer name
    def getName(self):
        return self.name

    # Setter method for customer gender
    def setGender(self, gender):
        self.gender = gender

    # Getter method for customer gender
    def getGender(self):
        return self.gender

    # Setter method for customer email
    def setEmail(self, email):
        self.email = email

    # Getter method for customer email
    def getEmail(self):
        return self.email

    # Setter method for customer phone number
    def setPhoneNumber(self, phone_number):
        self.phone_number = phone_number

    # Getter method for customer phone number
    def getPhoneNumber(self):
        return self.phone_number

    # Setter method for billing name
    def setBillingName(self, billing_name):
        self.billing_name = billing_name

    # Getter method for billing name
    def getBillingName(self):
        return self.billing_name

    # Setter method for credit card information
    def setCreditCardInfo(self, credit_card_info):
        self.credit_card_info = credit_card_info

    # Getter method for credit card information
    def getCreditCardInfo(self):
        return self.credit_card_info


# Class for handling payment details
class Payment:
    # Constructor for initializing payment attributes
    def __init__(self, payment_id="", amount=0.0, payment_method="", payment_status="Pending", transaction_date=""):
        self.payment_id = payment_id
        self.amount = amount
        self.payment_method = payment_method
        self.payment_status = payment_status
        self.transaction_date = transaction_date

    # Setter method for payment ID
    def setPaymentID(self, payment_id):
        self.payment_id = payment_id

    # Getter method for payment ID
    def getPaymentID(self):
        return self.payment_id

    # Setter method for payment amount
    def setAmount(self, amount):
        self.amount = amount

    # Getter method for payment amount
    def getAmount(self):
        return self.amount

    # Setter method for payment method
    def setPaymentMethod(self, payment_method):
        self.payment_method = payment_method

    # Getter method for payment method
    def getPaymentMethod(self):
        return self.payment_method

    # Setter method for payment status
    def setPaymentStatus(self, payment_status):
        self.payment_status = payment_status

    # Getter method for payment status
    def getPaymentStatus(self):
        return self.payment_status

    # Setter method for transaction date
    def setTransactionDate(self, transaction_date):
        self.transaction_date = transaction_date

    # Getter method for transaction date
    def getTransactionDate(self):
        return self.transaction_date

    # Method to process the payment
    def process_payment(self):
        print(f"Processing payment of {self.amount} via {self.payment_method}")


# Example scenarios for reservations, rooms, customers, and payments

# Scenario 1: Ali Al Mansoori at Emirates Palace
reservation1 = Reservation("20549876543", "Ali Al Mansoori", "ali.mansoori@uaemail.ae", "Emirates Palace Hotel", "Mon, Oct 1", "Wed, Oct 3")
room1 = Room("King Suite", 1, 2, 1200.75)
customer1 = Customer("Ali Al Mansoori", "Male", "ali.mansoori@uaemail.ae", "0501234567", "Ali H Al Mansoori", "Mastercard [ending in 1234]")
payment1 = Payment("98765", 2401.50, "Visa", "Completed", "2024-09-24")

# Scenario 2: Fatima Al Zahrani at Jumeirah Beach Hotel
reservation2 = Reservation("30587451234", "Fatima Al Zahrani", "fatima.zahrani@uaemail.ae", "Jumeirah Beach Hotel", "Fri, Nov 12", "Sun, Nov 14")
room2 = Room("Deluxe Room", 2, 3, 850.50)
customer2 = Customer("Fatima Al Zahrani", "Female", "fatima.zahrani@uaemail.ae", "0559876543", "Fatima A Zahrani", "Visa [ending in 5678]")
payment2 = Payment("87654", 5103.00, "Visa", "Pending", "2024-09-25")

# Scenario 3: Khalid Al Fahim at The Ritz-Carlton
reservation3 = Reservation("10547890234", "Khalid Al Fahim", "khalid.fahim@uaemail.ae", "The Ritz-Carlton", "Wed, Dec 8", "Fri, Dec 10")
room3 = Room("Executive Suite", 1, 2, 1750.00)
customer3 = Customer("Khalid Al Fahim", "Male", "khalid.fahim@uaemail.ae", "0546789012", "Khalid F Al Fahim", "Mastercard [ending in 4321]")
payment3 = Payment("23456", 3500.00, "Mastercard", "Completed", "2024-09-26")

# Scenario 4: Ayesha Al Shehhi at Fairmont Bab Al Bahr
reservation4 = Reservation("40567891011", "Ayesha Al Shehhi", "ayesha.shehhi@uaemail.ae", "Fairmont Bab Al Bahr", "Sat, Sep 18", "Mon, Sep 20")
room4 = Room("Standard Room", 1, 2, 600.25)
customer4 = Customer("Ayesha Al Shehhi", "Female", "ayesha.shehhi@uaemail.ae", "0558765432", "Ayesha S Al Shehhi", "Visa [ending in 9876]")
payment4 = Payment("76543", 1200.50, "Visa", "Completed", "2024-09-27")

# Display function
def display_info(customer, reservation, room, payment):
    # Display Customer details
    print("Customer Information")
    print(f"Name: {customer.getName()}, Gender: {customer.getGender()}")
    print(f"Email: {customer.getEmail()}, Phone: {customer.getPhoneNumber()}")
    print(f"Billing Name: {customer.getBillingName()}, Credit Card: {customer.getCreditCardInfo()}")
    print()

    # Display Reservation details
    print("Reservation Information")
    print(f"Reservation ID: {reservation.getReservationID()}")
    print(f"Hotel Name: {reservation.getHotelName()}")
    print(f"Check-in: {reservation.getCheckIn()}, Check-out: {reservation.getCheckOut()}")
    print()

    # Display Room details
    print("Room Information")
    print(f"Room Type: {room.getRoomType()}, Number of Rooms: {room.getNumberOfRooms()}")
    print(f"Nights: {room.getNights()}, Room Cost per Night: {room.getRoomCost()}")
    print(f"Total Room Charges: {room.calculate_total_charges()}")
    print()

    # Display Payment details
    print("Payment Information")
    print(f"Payment ID: {payment.getPaymentID()}")
    print(f"Amount: {payment.getAmount()}, Payment Method: {payment.getPaymentMethod()}")
    print(f"Payment Status: {payment.getPaymentStatus()}, Transaction Date: {payment.getTransactionDate()}")
    print("-" * 50)  # Separator for readability
    print()

# Display all four scenarios
display_info(customer1, reservation1, room1, payment1)
display_info(customer2, reservation2, room2, payment2)
display_info(customer3, reservation3, room3, payment3)
display_info(customer4, reservation4, room4, payment4)
