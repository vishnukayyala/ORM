# Ex03 Django ORM Web Application
## Date: 18/09/2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM
### models.py
```
from django.db import models
from django.contrib import admin
class Bank(models.Model):
    customer_id = models.IntegerField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)  
    monthly_interest = models.DecimalField(max_digits=5, decimal_places=2)  
    due_date = models.DateField()

class Loandetails(admin.ModelAdmin):
    list_display= ('customer_id','customer_name','account_type','loan_amount','monthly_interest','due_date')
```

### admin.py
```
from django.contrib import admin
from .models import Bankloan,BankloanAdmin
admin.site.register(Bankloan,BankloanAdmin)
```
## OUTPUT
![image](https://github.com/user-attachments/assets/dce924db-e64a-43da-b096-4c69c2812d14)
![image](https://github.com/user-attachments/assets/a96aae38-7188-47a4-9770-e82033bde282)
![image](https://github.com/user-attachments/assets/fd38983b-5488-42cf-93e3-ab9b31dd6917)

## RESULT
Thus the program for creating a database using ORM hass been executed successfully
