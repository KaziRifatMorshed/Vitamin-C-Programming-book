# Structure & Union

# typedef struct

# Do not get confused

In C and C++, two different operators are used for calling methods: you use `.` if you’re calling a method on the object directly and `->` if you’re calling the method on a pointer to the object and need to dereference the pointer first.\
In other words, if object is a pointer, `object->something()` is similar to `(*object).something()`.
