# Ex01 Django ORM Web Application
## Date: 28-11-2025

## AIM
To develop a Django Application to store and retrieve data from a E-Commerce Website Database for Amazon or Flipkart using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM



## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM
```from django.contrib import admin
from .models import Product

class ProductAdmin(admin.ModelAdmin):
    list_display = ('product_id', 'name', 'category', 'brand', 'price', 'stock', 'rating')
    search_fields = ('name', 'category', 'brand')
    list_filter = ('category', 'brand')
    ordering = ('product_id',)

admin.site.register(Product, ProductAdmin)```

```from .models import Product
   class Product(models.Model):
    product_id = models.AutoField(primary_key=True)
    name = models.CharField(max_length=200)
    category = models.CharField(max_length=100)
    brand = models.CharField(max_length=100)
    price = models.DecimalField(max_digits=10, decimal_places=2)
    stock = models.IntegerField()
    rating = models.FloatField(default=0.0)
    created_at = models.DateTimeField(auto_now_add=True)

    def _str_(self):
        return self.name```


## OUTPUT

<img width="1907" height="915" alt="Screenshot 2025-11-28 201754" src="https://github.com/user-attachments/assets/fe3ef7e3-16f8-4482-a15d-cbba39fb9855" />


## RESULT
Thus the program for creating E-commerce website database using ORM hass been executed successfully
