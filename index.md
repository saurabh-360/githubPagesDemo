[Login](#LoginUser)

[Logout](#LogoutUser)

[Home](#Home)



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
  



# Home
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
  

