# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

 ER diagram
 ![GitHub Logo](/images/entity.png)

## DESIGN STEPS

### STEP 1:
clone the github repository
### STEP 2:
start a new app
### STEP 3:
enter the code in admin.py and models.py


## PROGRAM

models.py
```
from django.db import models
from django.contrib import admin
# Create your models here.
class Student (models.Model):
referencenumber=models.CharField(max_length=20,help_text="reference number")
name=models.CharField(max_length=100)
age=models.IntegerField()
email=models.EmailField()
class StudentAdmin(admin.ModelAdmin):
list_display=('referencenumber','name','age','email')
```
admin.py
```
from django.contrib import admin
from .models import Student,StudentAdmin
# Register your models here.
admin.site.register(Student,StudentAdmin)
```
## OUTPUT

![GitHub Logo](/images/server.png)
![GitHub Logo](/images/table.png)


## RESULT
Successfully! Created Django ORM