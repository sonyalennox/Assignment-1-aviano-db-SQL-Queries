# Assignment-1-aviano-db-SQL-Queries - Sonya Lennox
#
1. Find all vehicles
  - SELECT
    - id,
    - brand,
    - model,
    - model_year,
    - mileage,
    - color,
    - vehicle_type_id,
    - current_location_id
  - FROM
    - vehicle
2. Find all vehicles with a mileage greater than 5000
  - SELECT
    - id,
    - brand,
    - model,
    - model_year,
    - mileage,
    - color,
    - vehicle_type_id,
    - current_location_id
  - FROM
    - vehicle
  - WHERE
    - mileage > 50000
3. Find id, model, and model_year of all vehicles that are white
  - SELECT
    - id,
    - model,
    - model_year
  - FROM
    - vehicle
  - WHERE
    - color = 'white'
4. Find all vehicles, listing them from newest to oldest
  - SELECT
    - id,
    - brand,
    - model,
    - model_year,
    - mileage,
    - color,
    - vehicle_type_id,
    - current_location_id
  - FROM
    - vehicle
  - ORDER BY
    - model_year DESC
5. Using the COUNT() function, find the number of vehicles made before 2018
  - SELECT
    - COUNT(*)
  - FROM
    - vehicle
  - WHERE
    - model_year < 2018
6. Add a new car to vehicle with the following information
  - INSERT INTO
    - vehicle
  - VALUES
    - (7,
    - 'Jeep',
    - 'Compass',
    - 2019,
    - 10000,
    - 'Rebecca_Purple'
    - 4,
    - 2);
7. Update the mileage on the Hyundai Elantra (id is 4) to 54256
  - SELECT
    - vehicle
  - SET
    - mileage = "54256"
  - WHERE
    - id = '4'
8. The company has decided to change the names of their insurence plans. Using the REPLACE() function, change all occurances of the word Cover to Insure.
  - SELECT
    - insurance
  - SET
    - name = REPLACE(name,'Cover','Insure')
  - WHERE
    - name IS NOT null;
9. A hobby of the Aviano owners is tax fraud. Delete all rental invoices that have a total_amount_payable greater that $3000
  - DELETE FROM
    - rental_invoice
  - WHERE
    - total_amount_payable > 3000
10. Using INNER JOIN, find that start_date, customer_id, first_name and last_name of all rentals made by the customer with an email of khumphriss@xrea.com
  - SELECT
    - start_date,
    - customer_id,
    - first_name,
    - last_name
  - FROM
    - customer
  - INNER JOIN
    - rental AS r
  - ON
    - customer_id = r.customer_id
  - WHERE
    - email = "khumphriss@xrea.com"
