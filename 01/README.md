### Slices



##### Range copies by value

---



```go
for i, v := range items {
	v = new_value	// won't change the underlying array
}
```



##### A slice is a view

---

- A slice does not own any data.
- A slice simply defines a view into some part of an array. 
- Append(Slice, Value) may force a construction of a new array.

```go
func (T any) append_gaurd(slice []T, val T) {
    if len(slice) == cap(slice)
    	// Throw Expection
    slice = append(slice, val)
}
```



##### An array is initiated with zeros

---



```go
func main() {
    arr := make([100]int)
    fmt.Println(arr)	// prints 100 zeros
}
```

