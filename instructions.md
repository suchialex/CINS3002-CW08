# Instructions

<details>
  <summary>
    💡 REPL/PyCharm Guide
  </summary>

  - To toggle commenting, highlight the line(s) and press Ctrl + /
  - To move a statement or block of statements one indent to the right, highlight the statement(s)  press Tab
  - To move a statement or block of statements one indent to the left, highlight the statement(s)  press Shift+Tab
  - Avoid using backspaces or spaces to remove or place indents
  - REPL Comments
    - To ask the instructor a code question, highlight the line(s) of code and press Alt + / and type in your question/issue/comment and click on collapse
    - To view comments placed by the instructor click on the comment icon at the end of any highlighted code
    - If your issue is resolved, click on Resolve to remove the comment
</details>


<details>
  <summary>
    Assignment Instructions
  </summary>

- In this assignment we manage product data using classes and **storing these class objects in a dictionary**
- Each product object has four data elements - Name, Price, Quantity
- All such product objects are stored in a dictionary whose keys will be the product ID
</details>


## Start Working

<details>
  <summary>
    ✅ Create a new PyCharm project
  </summary>

  - Create a new PyCharm project in a folder of your choice
  - Create a Python file - main.py
  - Inside the project create a new folder **cw08**
  - Create files classes.py, class_functions.py and validations.py
</details>

<details>
  <summary>
    ✅ Copy code from cw07
  </summary>

  - Copy the code in main.py and validations.py from CW07
  - Copy the code from dict_functions (modify these instead of writing them from scratch)
  - Change the import statement in main.py to use class_functions module in cw08
  - **Instructor will not provide employee data file**, it will be created using your program's `Add Product` option (_after you write code for that function_)
</details>

## In classes.py

<details>
  <summary>
    ✅ Define a class called product
  </summary>

  - Use coding conventions for class name
</details>


<details>
  <summary>
    ✅ Define __init__() for the product class
  </summary>

  - Because our product has three data fields, accept three parameters in the \_\_init\_\_ definition ⏩ 10-3a (private attributes)
  - 🚩 Do not forget the default parameter
  - Bind the product data parameters to the object using self assingment. Ensure these are private attributes.
</details>

<details>
  <summary>
    ✅ Define __str__() for the product class ⏩ 10-4a
  </summary>

  - 🚩 Do not forget the default parameter in the definition
  - Inside the \_\_str\_\_() function body
    - Write a statement that returns a formatted string as follows
    - Make sure to use the private attributes you created in the \_\_init\_\_() in the appropriate placeholders

  Name: <product_name>  
  Price: <product_price>  
  Quantity: <product_qty>  

</details>

<details>
  <summary>
    ✅ Define accessor method get_name() in the product class ⏩ 10-5a
  </summary>

  - 🚩 Do not forget the default parameter in the definition
  - Inside the get_name function body
    - Write a statement that returns the private attribute for the product name
</details>

<details>
  <summary>
    ✅ Define accessor methods get_price, get_qty in the product class
  </summary>

  - Return the appropriate private attribute in each method
</details>


<details>
  <summary>
    ✅ Define mutator method set_name() in the product class ⏩ 10-6a
  </summary>

  - Accept the new name (choose a name for this new name) as a parameter
  - 🚩 Do not forget the default parameter in the definition
  - Inside the set_name function body
    - Write a statement that assigns this new name to the existing private attribute for the product name
</details>

<details>
  <summary>
    ✅ Define mutator methods set_price and set_qty in the product class
  </summary>

  - Return the appropriate private attribute in each method
</details>

## In class_functions.py

<details>
  <summary>
    ✅ Imports
  </summary>

  - Using the from keyword, import the product class you created in classes module
  - Fix the import existing import statement to use validations from cw08 instead of cw07
</details>

<details>
  <summary>
    ✅ Modify file_to_dictionary()
  </summary>

  - In the body of file_to_dictionary, change the file location to `cw08/products.bin`
</details>

<details>
  <summary>
    ✅ Modify product_operations()
  </summary>

  - Comment out all the code except the file_to_dictionary call
  - Print the dictionary (it should print empty dictionary, if you have used exception handling in that function)
</details>


<details>
  <summary>
    ✅ Modify add_product()
  </summary>

  - 💡 We can use the same function generate_product_id_dict() we wrote in validations.py (because products is still a dictionary)
  - After the code to get all the product data fields, create an object of the Product class named `new_product` by passing them in the same order as used in the initializer method  
  - To the products dictionary add a new key/value pair
    - key is the calculated product ID and
    - value is new product object
  - Print `Added Product`
  - Return products dictionary (optional if you decide to keep the dictionary name the same in all functions)

</details>

<details>
  <summary>
    ✅ Modify dictionary_to_file()
  </summary>

  - In the body of dictionary_to_file(), change the file location to `cw08/products.bin`
</details>


<details>
  <summary>
    ✅ Call add_product()
  </summary>
  
  - In product_operations() function, uncomment whatever code you need to call
    - add_product()
    - **and dictionary_to_file()**
  - Execute the program and add a new employee and Exit out of the program
  - If your code is correct, a new file called products.bin will be created in cw08 folder and will have some un-readable data
</details>



<details>
  <summary>
    ✅ Modify lookup_product()
  </summary>
  
  - Delete the print statement(s) in the if block and simply print the product object at the key provided by the user
  - This print statement will call the \_\_str\_\_() method and print all the data correctly
  
</details>

<details>
  <summary>
    ✅ Call lookup_product() after add_product()
  </summary>

  - In product_operations() function, uncomment whatever code you need to call lookup_product
  - 📜 Test your code with the most recently added product ID
</details>


<details>
  <summary>
    ✅ Modify modify_name()
  </summary>

  - Inside the if block,
  - We find the appropriate dictionary element using product_id (converted to integer) as the key and store it in a variable, say `found_product`
  - Using this found_product object, call the set_name method by passing the new name as argument ⏩ 10-6b
</details>
</details>


<details>
  <summary>
    ✅ Call modify_name()
  </summary>

  - In product_operations() function, uncomment whatever code you need to call modify_name()
  - Test your code and make sure product name is being modified correctly
</details>


<details>
  <summary>
    ✅ Same for modify_price, modify_quantity
  </summary>

  - Do the same steps as above for modifying price and quantity by calling the appropriate set methods (aka mutator methods) defined in the class
</details>


<details>
  <summary>
    ✅ Modify display_products()
  </summary>

  - Inside the for loop
    - Get each data element using the loop variable (product object) and the appropriate get methods
    - For example, product name would be  `<loop_variable>.get_name()` ⏩ 10-5b
    - Do the same for other data elements - price and quantity
  - Display all these values in a tabular format
  - You may choose column widths and alignment to fit your data

</details>


<details>
  <summary>
    ✅ Call  display_products()
  </summary>

  - Uncomment appropriate code in product_operations function to call display_products()
  - Test your code to make sure the product(s) are being displayed correctly
</details>


<details>
  <summary>
    ✅ No action on delete_product()
  </summary>

  - Nothing to change here, because we still have to delete an product by deleting the dictionary element, which in this assignment is an object (it was a dictionary in the previous assignment)
</details>



<details>
  <summary>
    ✅ Call  delete_product()
  </summary>

  - Uncomment code in product_operations to call delete_product()
  - 📜 Execute your code and ensure ALL product operations are being performed correctly
</details>


## Copy code to replit

<details>
  <summary>
    ✅ Copy code to replit
  </summary>
  
  - Copy the contents of classes.py, validations.py and class_functions.py to replit under folder cw08
  - Upload your products.bin (it will NOT upload to cw08, you have to drag and drop it) or execute code and Add Product to create a new products.bin file
  - Comment out the existing import statement and code in main function body
  - Copy the import statement and code from main.py in your PyCharm Project and paste it in the appropriate places in replit
  - Submit the URL on Canvas assignment
</details>
