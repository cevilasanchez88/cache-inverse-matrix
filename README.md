# # Programming assignment week 3 R programming
# # caching the inverse of a matrix
# # As it is said in the order of the assignment this function creates a special "matrix" object that can cache its inverse.

# makeCacheMatrix <- function(x = matrix()) {
#   inv <- NULL
#   set <- function(y) {
#     x <<- y
#     inv <<- NULL
#   }
#   get <- function() x
#   setInverse <- function(inverse) inv <<- inverse
#   getInverse <- function() inv
#   list(set = set,
#        get = get,
#        setInverse = setInverse,
#        getInverse = getInverse)
# }
# 
# 
# # The next function calculates the inverse of the matrix given. (Using also the function names proposed by professor Peng)
# 
# cacheSolve <- function(x, ...) {
#   ## Return a matrix that is the inverse of 'x'
#   inv <- x$getInverse()
#   if (!is.null(inv)) {
#     message("getting cached data")
#     return(inv)
#   }
#   mat <- x$get()
#   inv <- solve(mat, ...)
#   x$setInverse(inv)
#   inv
# }
