# Ex02 Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a student database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![image](https://user-images.githubusercontent.com/121165979/233148181-b66f57d0-b64f-4b56-9f11-583b9a36bae2.png)


## DESIGN STEPS

### STEP 1:
clone the repository from github.

### STEP 2:
create an admin interface for django.

### STEP 3:
create an app and edit settings.py

### STEP 4:
make migrations and migrate the changes

### STEP 5:
create admin user and write python code for admin and models.

### STEP 6:
make all the migrations to 'myapp'.

### STEP 7:
create an student database with 10 fields using runserver command.

## PROGRAM
```python
admin.py

from django.contrib import admin
from.models import student,studentAdmin
admin.site.register(student,studentAdmin)

models.py

from django.db import models
from django.contrib import admin
class student(models.Model):
    sid=models.CharField(max_length=200)
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class studentAdmin(admin.ModelAdmin):
    list_display=('sid','name','salary','age','email')
    
```

## OUTPUT
![ORM](https://user-images.githubusercontent.com/120554177/234289744-5b2ed9ae-1ae8-4a2d-952a-f80812438834.png)


## SERVER OUTPUT
![so](https://user-images.githubusercontent.com/120554177/234290043-a0254369-40e3-4e84-9d7f-9ab0dc43cf39.png)

## RESULT
The program for creating an student database using ORM is executed sucessfully.
