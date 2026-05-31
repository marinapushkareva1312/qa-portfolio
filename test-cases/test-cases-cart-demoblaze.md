# Test Cases: Cart — demoblaze.com

**Tester:** Marina Pushkareva  
**Date:** 2026-05-31  
**Application:** STORE (demoblaze.com)  
**Feature:** Shopping Cart  
**Environment:** Browser (Firefox/Chrome), Desktop

-----

## Scope

Testing the Cart functionality — adding products, viewing cart contents, deleting items, and placing an order.

**Elements under test:**

- “Add to cart” button on product page
- Cart page (accessed via “Cart” in nav bar)
- Delete button for items in cart
- Place Order button and order form

-----

## Test Cases

|TC ID|Title                              |Preconditions                |Steps                                                                                                                 |Expected Result                                                      |Status|
|-----|-----------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|------|
|TC-01|Add one product to cart            |User is on any product page  |1. Open any product<br>2. Click **Add to cart**                                                                       |Confirmation alert appears, product is added to cart                 |-     |
|TC-02|Added product appears in cart      |Product has been added       |1. Click **Cart** in nav bar                                                                                          |Cart page shows the added product with name, price, and delete option|-     |
|TC-03|Add multiple different products    |User is on the site          |1. Add product A<br>2. Add product B<br>3. Open Cart                                                                  |Both products appear in cart                                         |-     |
|TC-04|Total price is calculated correctly|2+ products in cart          |1. Add two products<br>2. Open Cart<br>3. Check total                                                                 |Total equals the sum of all product prices                           |-     |
|TC-05|Delete one product from cart       |Cart has 2+ products         |1. Open Cart<br>2. Click **Delete** next to one product                                                               |Product is removed, remaining products stay, total updates           |-     |
|TC-06|Delete all products from cart      |Cart has products            |1. Open Cart<br>2. Delete each product one by one                                                                     |Cart becomes empty                                                   |-     |
|TC-07|Place order with valid data        |Cart has at least one product|1. Open Cart<br>2. Click **Place Order**<br>3. Fill in Name, Country, City, Card, Month, Year<br>4. Click **Purchase**|Success confirmation message appears with order details              |-     |
|TC-08|Place order with empty Name field  |Cart has a product           |1. Open Cart<br>2. Click **Place Order**<br>3. Leave Name empty<br>4. Click **Purchase**                              |Error message or validation warning is shown                         |-     |
|TC-09|Place order with empty Card field  |Cart has a product           |1. Open Cart<br>2. Click **Place Order**<br>3. Leave Credit card empty<br>4. Click **Purchase**                       |Error message or validation warning is shown                         |-     |
|TC-10|Place order with all fields empty  |Cart has a product           |1. Open Cart<br>2. Click **Place Order**<br>3. Leave all fields empty<br>4. Click **Purchase**                        |Error message is shown, order is not placed                          |-     |
|TC-11|Open empty cart                    |No products added            |1. Click **Cart** in nav bar                                                                                          |Cart page opens and shows no items, total is $0                      |-     |
|TC-12|Cart persists after page refresh   |Product added to cart        |1. Add a product to cart<br>2. Refresh the page<br>3. Open Cart                                                       |Product is still in cart after refresh                               |-     |

-----

## Notes

- TC-07 requires a test credit card number (any number is accepted on demo sites)
- Status column: Pass / Fail / Blocked — to be filled during test execution
- Priority: TC-01, TC-02, TC-04, TC-07 are high priority (core purchase flow)