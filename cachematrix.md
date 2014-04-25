### Introduction

Here there are two functions for creating the inverse of a Matrix

*  `makeCacheMatrix`: This function creates a special "matrix" object
    that can cache its inverse.

1.  set the value of the matix
2.  get the value of the matrix
3.  set the value of the inverse of the matrix
4.  get the value of the matrix
 
* `cacheSolve`: This function computes the inverse of the special
    "matrix" returned by `makeCacheMatrix` above. If the inverse has
    already been calculated (and the matrix has not changed), then
    `cacheSolve` should retrieves the inverse from the cache.

### Example of using: Creating the inverse of the matrix

First we call `makeCacheMatrix` passing the matrix as an argument:

`matriz<-matrix(1:4,2,2)`
        > matriz
            [,1] [,2] 
        [1,]    1    3
        [2,]    2    4

`invertido <- makeCacheMatrix(matriz)`

`resultado<-cacheSolve(invertido)`
        > resultado
             [,1] [,2]
        [1,]   -2  1.5
        [2,]    1 -0.5
 
Firts time calculates the result, but second time goes for the result 
to cache:

        > resultado2<-cacheSolve(invertido)
        getting cached data
        > resultado2
             [,1] [,2]
        [1,]   -2  1.5
        [2,]    1 -0.5
