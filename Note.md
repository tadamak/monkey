# Chapter1

struct literal
```go
type Point struct {X, Y int} // X, Yはpublic
p := Point{Y: 10} // Xはゼロ値
q := Point{5, 2}
```

method宣言
```go
// Point型のmethod
func (p Point) Distance(q Point) float64 {
    ...
}
```
* p => receiver
* p.Distance => selector

無名structがある。
宣言しつつ構造体リテラルで初期化する形になる。
```go
p := &struct {X, Y int} {10, 3}
fmt.Printf("%d\n", p.X)
```

arrayとかsliceとか
* arrayは値そのもの
* sliceは部分列の参照
* arr[:]でarrayからsliceを作れる
* arrayだと思って初期化していたものがsliceだったらしい？
