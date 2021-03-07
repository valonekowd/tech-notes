* A window function always performs the calculation on the result set
    * After the `JOIN`, `WHERE`, `GROUP BY` and `HAVING` clause
    * Before the `final ORDER BY` clause in the evaluation order
* Syntax
	* window_function(arg1, arg2, …)  OVER  (
		[ PARTITION  BY  partition_expression ]
		[ ORDER  BY  sort_expression  [ ASC  |  DESC ] [NULLS  { FIRST  |  LAST } ]
	)

        * window_function
            * Some aggregate functions such as `COUNT(), SUM(), AVG(), MIN(), MAX()` can be also used  as window functions
            * `ROW_NUMBER()`
            * `RANK()`
            * `DENSE_RANK()`
            * `LAG()` —> access data from the previous row(s)
            * `LEAD()` —> access data from the next row(s)
            * …
        * PARTITION BY
            * Divides rows into multiple groups or partitions to which the window function is applied
            * Optional —> If you skip the `PARTITION BY` clause, the window function will treat the whole result set as a single partition
        * ORDER BY
            * Specifies the order of rows in each partition to which the window function is applied
            * Uses the `NULLS FIRST` or `NULLS LAST` option to specify whether nullable values should be first or last in the result set. The default is `NULLS LAST` option
        * frame_clause
            * { RANGE  |  ROWS  | GROUPS  }  frame_start  [ frame_exclusion ]
            * { RANGE  |  ROWS  | GROUPS  }  BETWEEN  frame_start  AND  frame_end  [ frame_exclusion ]
        * WINDOW clause —> re-use multiple times in `SELECT` clause
