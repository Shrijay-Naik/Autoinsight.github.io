# AutoInsight - Car Repair Service Platform

class Service:
    def __init__(self, name, base_price, sustainability_factor=1.0):
        self.name = name
        self.base_price = base_price
        self.sustainability_factor = sustainability_factor

    def calculate_price(self):
        return self.base_price * self.sustainability_factor

class Customization:
    def __init__(self, description, price):
        self.description = description
        self.price = price

class CustomerRequest:
    def __init__(self, service, customizations=[]):
        self.service = service
        self.customizations = customizations

    def total_price(self):
        total = self.service.calculate_price()
        for custom in self.customizations:
            total += custom.price
        return total

# Sample Services
basic_service = Service(name="Basic Maintenance", base_price=8000)
advanced_service = Service(name="Advanced Repair", base_price=20000)
premium_service = Service(name="Full Sustainability Package", base_price=40000, sustainability_factor=1.2)

# Sample Customizations
custom1 = Customization("Eco-Friendly Parts", 3000)
custom2 = Customization("Extended Warranty", 5000)
custom3 = Customization("Performance Tuning", 7000)

# Customer Request
customer_request = CustomerRequest(service=premium_service, customizations=[custom1, custom2])
print("Total Service Cost:", customer_request.total_price())

# Executive Team Details
class Executive:
    def __init__(self, role, name, email=None, phone=None, picture=None):
        self.role = role
        self.name = name
        self.email = email
        self.phone = phone
        self.picture = picture

# Adding Executives
ceo = Executive(role="CEO", name="John Doe", email="ceo@autoinsight.com", phone="123-456-7890", picture="path/to/ceo.jpg")
cfo = Executive(role="CFO", name="Jane Smith", picture="path/to/cfo.jpg")
cto = Executive(role="CTO", name="Alice Johnson", picture="path/to/cto.jpg")

# Display Executives
executives = [ceo, cfo, cto]
for exec in executives:
    print(f"{exec.role}: {exec.name}")
    if exec.email:
        print("Email:", exec.email)
    if exec.phone:
        print("Phone:", exec.phone)
    if exec.picture:
        print("Picture Path:", exec.picture)
