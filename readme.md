# Laravel Seeder File for Top Fashion Designers in the World
#### This can only work with laravel unless you intend to extract the designer's name and use in different project

This seeder file was created for a client's project I worked on recently, the file contains a standard laravel seeder file you can use to populate your database

## How to Use
#### Step 1: Create the model and migration files in laravel

```
    php artisan make:model Designer -m
```


#### Step 2: Add relevant columns to Designer model migration file

```
    $table->id();
    $table->string('uid')->unique(); // optional unless you want to use the DesignerSeederAlt.php file
    $table->string('designer_name');
```



#### Step 3: Copy Seeder file to designated folder

After the "Designer" model is created, you can copy the file "DesignerSeeder.php" into your laravel seeder folder ./your_laravel_project_root/database/seeders

```
   sudo cp DesignerSeeder.php ./your_laravel_project_root/database/seeders
```


#### Step 4: Run Laravel migration command

```
    php artisan migrate
```

### Important
Please note the only difference between "DesignerSeederAlt.php" file and "DesignerSeeder.php" is the seperate column for "uid" in "DesignerSeederAlt.php"