  
# Foo
jhkhkjh
hjkjh
hkjhj
<div id="section1">
  <h1>Section 1</h1>
  <p>Section 1 content</p>
  <div id="section1-1">
    <h2>Section1-1</h2>
    <p>section 1-1 content</p>
  </div>
    <div id="section1-2">
    <h2>Section1-2</h2>
    <p>section 1-2 content</p>
  </div>
</div>



<h1>Section 1</h1>
<p>Section 1 content</p>
<h2>Section1-1</h2>
<p>section 1-1 content</p>
<h2>Section1-2</h2>
<p>section 1-2 content</p>



 <details>
      <summary>Your header here! (Click to expand)</summary>
      Your content here...</br>
      (markup only where supported)</br>
      more content here...</br>
  [Foo](#foo)




**Login User**
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
    **Content:** `{ id : 12, name : "Michael Bloom", other Personal info: {list} }`
 
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
  
  
</details>
