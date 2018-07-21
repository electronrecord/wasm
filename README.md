This is a repo with my starting point in learning Web Assembly.

So here there is i think the simplest example to run a wasm function under node,
and also in browser - a fibonaci function execution once in js and then in wasm.

For node example, after creating the file main.wat which is the declaration of a simple function
which returns 42, we run node ./scripts/build/index.js to compile from main.wat to main.wasm,
and then we can run node app.js to test the wasm function.


/* Fibonaci example */

To compile fib.ts file, which has the wasm code in ts format, we run this

$ asc fib.ts -o fib.wasm

$ http-server

in console, type fib(5) and we should see the result.

To compare the speed between js and wasm function compilation,
we can type in browser console:

timer(simpleFib, 99999)

and then

timer(fib, 99999)
