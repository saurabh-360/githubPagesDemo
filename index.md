[Login](#login)

[Logout](#logout)

[Home](#home)



# Login
----
  Validates & Returns json data about a single user.
  
* **URL**

  /login

* **Method:**

  `POST`
  
*  **URL Params**

   **Required:**
 
   * `email=[String]`   
   * `password=[String]`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ id : 12, name : "Michael Bloom", token: "accessToken", other Personal info: {list} }`
 
* **Error Response:**

  * **Code:** 400 NOT FOUND <br />
    **Content:** `{ error : "email/password is incorrect" }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:**

     ```
     {
	      error : "You are unauthorized to make this request,
   		  depending on the oauth process we use(if any)." 
     }
     ```

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/login",
      dataType: "json",
      type : "POST",
      success : function(r) {
        console.log(r);
      }
    });
  ```
  


# Logout
----
  Validates & Returns json data about a single user.
  
* **URL**

  /logout
* **Method:**
  `POST`
  
*  **URL Params**

   **Required:**
 
   * `accessToken=[String]`   

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{ success : "logged out successfully." }`
     
* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/logout",
      dataType: "json",
      type : "POST",
      success : function(r) {
        console.log(r);
      }
    });
  ```
  

# Home
----
  Validates & Returns json data about a single user.
  
* **URL**

  /home

* **Method:**

  `POST`
  
*  **URL Params**

   **Required:**
 
   * `accessToken=[String]`   
   * `userId=[String]`

* **Data Params**

  None

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** 

    ```
    {
   categories:[
	    {id: 1, "title":"wash", id: 1, "title":"wash"},
		 {id: 1, "title":"wash", id: 1, "title":"wash"}
	 	], 
	banners: [{"key value pairs"}]
 ```
* **Error Response:**

  * **Code:** 400 NOT FOUND <br />
    **Content:** `{ error : "No Data Found." }`

  OR

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:**

     ```
     {
	      error : "You are unauthorized to make this request,
   		  depending on the oauth process we use(if any)." 
     }
     ```
