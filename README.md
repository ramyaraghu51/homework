## Elixir SDET homework assignment

The tests focus on negative testing the account creation on facebook. I tried to login to https://www.facebook.com/, but facebook website stated that the current browser that I use in automation is not supported and kept on redirecting me to m.facebook.com. I took the following steps to avoid redirect.
In the config file, I set the config :hound, http: [{ "follow_redirect", false}] http: [{ "follow_redirect", false}] and tried settin max forward to 1. None of the attempts to avoid redirect worked, So I have developed the test cases for account creation in m.facebook.com. 

## Test Cases

1. Name : Invalid first name and last name. 
      1. Input : 1.first name field empty once with valid last name and  2. last name field empty with valid first name.
      2. Expected Result : Error message "Please enter valid First name" or "Please enter valid last name" 
      3. Actual Result: Error message "Please enter valid First name" when first name field is nil" "Please enter valid last name" when last name field is nil."

2. Name : Invalid date of birth Input: 
    1.  Date of birth in future. For eg, Oct 5,2022.
    2.   Expected Result: Error message "It looks like you entered the wrong info. Please be sure to use your real birthday." 
    3.   Actual Result : Error message "It looks like you entered the wrong info. Please be sure to use your real birthday.

3. Name :Invalid phone number
    1.  Inputs : 1. Phone number field empty 2. Phone number with 7 digits.
    2.  Expected Result: "Please enter a valid phone number" 
    3.  Actual Result : "Please enter a valid phone number"

4. Name : Invalid gender 
      1. Input : No gender is selected. 
      2.Expected Result : Please select your gender 
      3. Actual Result: Please select your gender.

5. Name : Invalid password 
      1.   Inputs : 1. Password field empty 2. Password with 3 characters less than the accepted limit. 
      2.   Expected Result : " Enter a combination of at least six numbers, letters and punctuation marks (like ! and &)." 
      3.  Actual Result : "Enter a combination of at least six numbers, letters and punctuation marks (like ! and &).")."
 


## Getting Up and Running

- Download the latest version of chromedriver and ensure that your version of chrome is up to date as well
- Run chromedriver
- In a different terminal window or tab, cd into the homework project and you can now execute the command "mix test" and it will run all of the test files in the "test" folder


