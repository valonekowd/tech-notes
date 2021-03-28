* Get the current date
  * `SELECT NOW()::DATE;`
  * `SELECT CURRENT_DATE;`
* Output a PostgreSQL date value in a specific format
  * `SELECT TO_CHAR(NOW()::DATE, 'dd/mm/yyyy');`
  * `SELECT TO_CHAR(NOW()::DATE, 'Mon dd, yyyy');`
* Get the interval between two dates
  * `SELECT NOW() - created_at AS diff`
* Calculate ages in years, months, and days
  * `SELECT AGE(birth_date) FROM employees;`
  * `SELECT AGE('2015-01-01', birth_date) FROM employees;`
* Extract year, quarter, month, week, day from a date value
  * `SELECT EXTRACT (YEAR FROM birth_date) AS YEAR FROM employees;`
  * `SELECT EXTRACT (MONTH FROM birth_date) AS MONTH FROM employees;`
  * `SELECT EXTRACT (DAY FROM birth_date) AS DAY FROM employees;`