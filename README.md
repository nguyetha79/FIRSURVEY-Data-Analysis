## Export data from MongoDB Atlas 

* Download [MongoDB Command Line Database Tools](https://fastdl.mongodb.org/tools/db/mongodb-database-tools-windows-x86_64-100.9.4.zip)

* Extract file and open command prompt in `bin` folder

* Export data as `BSON` file
    ```
    mongodump --uri mongodb+srv://nguyetha79:Nguyetha79*@cluster0.roptdmb.mongodb.net/test --out bson
    ```
    *`bson` folder in `bin` folder*

* Convert `BSON` to `CSV`

    Open Terminal
    - `mkdir bson`
    - Copy only `bson` files and paste them in this folder
    - `python bson2csv.py bson csv`

* Export data as `JSON` file:

    E.g: export collection `users`
    ```
    mongoexport --uri mongodb+srv://nguyetha79:Nguyetha79*@cluster0.roptdmb.mongodb.net/test --collection users --jsonArray --pretty --out json/users.json
    ```