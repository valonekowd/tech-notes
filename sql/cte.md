There are 3 ways to use `Common Table Expressions (CTEs)`
* Basic CTE

    * WITH  temp  AS  (
            SELECT  …  FROM  …
    )
    SELECT  …  FROM  …  WHERE  …  GROUP BY  …  ORDER BY  …

* Writable CTE
* Recursive CTE
    * WITH  RECURSIVE