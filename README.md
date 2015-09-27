#Readme.md


Use a function like this to test the cachematrix.R program.
------------------------------------
test = function(mat){
        ## @mat: an invertible matrix
        
        temp = makeCacheMatrix(mat)
        
        start.time = Sys.time()
        cacheSolve(temp)
        dur = Sys.time() - start.time
        print(dur)
        
        start.time = Sys.time()
        cacheSolve(temp)
        dur = Sys.time() - start.time
        print(dur)
}
----------------------------------

Executing would show the time difference when its cached.
mat1 = matrix(r, nrow=1000, ncol=1000)
test(mat1)

