# utl-drop-variables-whose-names-contain-any-of-several-substrings
Drop variables whose names contain any of several substrings.

    Drop variables whose names contain any of several substrings

    Problem: Drop variable names that contain either 'PP' or 'MEAN'

    github
    https://tinyurl.com/y8aggy3b
    https://github.com/rogerjdeangelis/utl-drop-variables-whose-names-contain-any-of-several-substrings

    https://tinyurl.com/y853dc3l
    https://github.com/rogerjdeangelis/utl-select-variables-whose-names-satisfy-a-regular-expression

    StackOverflow
    related to https://tinyurl.com/y9nfopmb
    https://stackoverflow.com/questions/53767526/dynamically-exclude-column-names-in-proc-sql-macro

    see for
    https://tinyurl.com/y9nfugth
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories

    I realize this is a dumb example and there are other ways to drop these variables,
    but the method provided  is more general

    Other methods
    drop LO: UP:
    drop LOWERMEAN -- UPPER

    varlist macro by
    Author: Søren Lassen, s.lassen@post.tele.dk


    INPUT
    =====

     SASHELP.CLASSFIT total obs=19                             RULE - DROP because 'PP' or 'MEAN'
                                                              -------------------------------------------
      NAME       SEX    AGE    HEIGHT    WEIGHT    PREDICT    LOWERMEAN    UPPERMEAN     LOWER      UPPER

      Joyce       F      11     51.3       50.5     56.993      43.804       70.182      29.883     84.103
      Louise      F      12     56.3       77.0     76.488      67.960       85.017      51.315    101.662
      Alice       F      13     56.5       84.0     77.268      68.907       85.630      52.150    102.386
     .....
      Ronald      M      15     67.0      133.0    118.208     110.771      125.645      93.383    143.034
      Alfred      M      14     69.0      112.5    126.006     116.942      135.071     100.646    151.367
      Philip      M      16     72.0      150.0    137.703     125.861      149.545     111.223    164.184


    EXAMPLE OUTPUT
    --------------

     WORK.CLASS total obs=19

      NAME       SEX    AGE    HEIGHT    WEIGHT    PREDICT

      Joyce       F      11     51.3       50.5     56.993
      Louise      F      12     56.3       77.0     76.488
      Alice       F      13     56.5       84.0     77.268
     .....
      Ronald      M      15     67.0      133.0    118.208
      Alfred      M      14     69.0      112.5    126.006
      Philip      M      16     72.0      150.0    137.703


    PROCESS
    =======

      data class;
        set sashelp.classfit
            (drop=%utl_varlist(sashelp.classfit,prx=/ER|MEAN/i));
      run;quit;

    OUTPUT
    ======
     see above

    No need to make data just use SASHELP.CLASSFIT


    Drop variables whose names contain any of several substrings

    Problem: Drop variable names that contain either 'PP' or 'MEAN'

    github
    https://tinyurl.com/y8aggy3b
    https://github.com/rogerjdeangelis/utl-drop-variables-whose-names-contain-any-of-several-substrings

    https://tinyurl.com/y853dc3l
    https://github.com/rogerjdeangelis/utl-select-variables-whose-names-satisfy-a-regular-expression

    StackOverflow
    related to https://tinyurl.com/y9nfopmb
    https://stackoverflow.com/questions/53767526/dynamically-exclude-column-names-in-proc-sql-macro

    see for
    https://tinyurl.com/y9nfugth
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories

    I realize this is a dumb example and there are other ways to drop these variables,
    but the method provided  is more general

    Other methods
    drop LO: UP:
    drop LOWERMEAN -- UPPER

    varlist macro by
    Author: Søren Lassen, s.lassen@post.tele.dk


    INPUT
    =====

     SASHELP.CLASSFIT total obs=19                             RULE - DROP because 'PP' or 'MEAN'
                                                              -------------------------------------------
      NAME       SEX    AGE    HEIGHT    WEIGHT    PREDICT    LOWERMEAN    UPPERMEAN     LOWER      UPPER

      Joyce       F      11     51.3       50.5     56.993      43.804       70.182      29.883     84.103
      Louise      F      12     56.3       77.0     76.488      67.960       85.017      51.315    101.662
      Alice       F      13     56.5       84.0     77.268      68.907       85.630      52.150    102.386
     .....
      Ronald      M      15     67.0      133.0    118.208     110.771      125.645      93.383    143.034
      Alfred      M      14     69.0      112.5    126.006     116.942      135.071     100.646    151.367
      Philip      M      16     72.0      150.0    137.703     125.861      149.545     111.223    164.184


    EXAMPLE OUTPUT
    --------------

     WORK.CLASS total obs=19

      NAME       SEX    AGE    HEIGHT    WEIGHT    PREDICT

      Joyce       F      11     51.3       50.5     56.993
      Louise      F      12     56.3       77.0     76.488
      Alice       F      13     56.5       84.0     77.268
     .....
      Ronald      M      15     67.0      133.0    118.208
      Alfred      M      14     69.0      112.5    126.006
      Philip      M      16     72.0      150.0    137.703


    PROCESS
    =======

      data class;
        set sashelp.classfit
            (drop=%utl_varlist(sashelp.classfit,prx=/ER|MEAN/i));
      run;quit;

    OUTPUT
    ======
     see above

    No need to make data just use SASHELP.CLASSFIT


    Drop variables whose names contain any of several substrings

    Problem: Drop variable names that contain either 'PP' or 'MEAN'

    github
    https://tinyurl.com/y8aggy3b
    https://github.com/rogerjdeangelis/utl-drop-variables-whose-names-contain-any-of-several-substrings

    https://tinyurl.com/y853dc3l
    https://github.com/rogerjdeangelis/utl-select-variables-whose-names-satisfy-a-regular-expression

    StackOverflow
    related to https://tinyurl.com/y9nfopmb
    https://stackoverflow.com/questions/53767526/dynamically-exclude-column-names-in-proc-sql-macro

    see for
    https://tinyurl.com/y9nfugth
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories

    I realize this is a dumb example and there are other ways to drop these variables,
    but the method provided  is more general

    Other methods
    drop LO: UP:
    drop LOWERMEAN -- UPPER

    varlist macro by
    Author: Søren Lassen, s.lassen@post.tele.dk


    INPUT
    =====

     SASHELP.CLASSFIT total obs=19                             RULE - DROP because 'PP' or 'MEAN'
                                                              -------------------------------------------
      NAME       SEX    AGE    HEIGHT    WEIGHT    PREDICT    LOWERMEAN    UPPERMEAN     LOWER      UPPER

      Joyce       F      11     51.3       50.5     56.993      43.804       70.182      29.883     84.103
      Louise      F      12     56.3       77.0     76.488      67.960       85.017      51.315    101.662
      Alice       F      13     56.5       84.0     77.268      68.907       85.630      52.150    102.386
     .....
      Ronald      M      15     67.0      133.0    118.208     110.771      125.645      93.383    143.034
      Alfred      M      14     69.0      112.5    126.006     116.942      135.071     100.646    151.367
      Philip      M      16     72.0      150.0    137.703     125.861      149.545     111.223    164.184


    EXAMPLE OUTPUT
    --------------

     WORK.CLASS total obs=19

      NAME       SEX    AGE    HEIGHT    WEIGHT    PREDICT

      Joyce       F      11     51.3       50.5     56.993
      Louise      F      12     56.3       77.0     76.488
      Alice       F      13     56.5       84.0     77.268
     .....
      Ronald      M      15     67.0      133.0    118.208
      Alfred      M      14     69.0      112.5    126.006
      Philip      M      16     72.0      150.0    137.703


    PROCESS
    =======

      data class;
        set sashelp.classfit
            (drop=%utl_varlist(sashelp.classfit,prx=/ER|MEAN/i));
      run;quit;

    OUTPUT
    ======
     see above

    No need to make data just use SASHELP.CLASSFIT


