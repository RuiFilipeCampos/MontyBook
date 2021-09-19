# MontyBook

A computational notebook for MontyCarlo projects.

# The plan.

- React front end
- Django Backend, two components:
  - main -> receives requests from the client and redirects them to a kernel
  - kernel -> receives requests from main and carries out processing

## Backend description

The `kernel` is meant to be its own process running in parallel with `main`. Several kernels may be spawn.

The `kernel` will use the `exec(the_code)` function call to execute the python code passed by `main`.

Secure channels will be established between `kernel` and `main` to prevent any sort of code injection.

## Front end description

MontyBook is meant for prototyping. 


```
---------------------------
-                         -
-                         -
-         PLOT            -
-                         -         
-                         -
------- draggable ---------
-                         -                         
- [form] [dens] [create]  -
-                         -
-  _____________________  -
-        geom code        -
-  _____________________  -
-          [ render geo]  -
-          [simulate]     -
-                         -
---------------------------
```





```JSON
{
  "name":"User defined name",
  
  "body":{
    "materials":[
        {
        "name":"Water(Liquid)", 
        "compiled":1, 
        "formula":{"H":2, "O":1}
        },
        ],
     "code":"#actual python code", 
     "sources": {},
     
  },
}
```

