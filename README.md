### tardisgo
---
https://github.com/tardisgo/tardisgo

```go
// tardisgo_test.go

func TestCore(t *testing.T) {
  err := os.Chdir("tests/core")
  if err != nil {
    t.Error(err)
  }
  
  *debugFlag = true
  err = doTestable([]string{"test.go"})
  if err != nil {
    t.Error(err)
  }
  
  out, err := exec.Command("haxe", "--main", "tardis.Go", "-cp", "tardis", "--interp").CombineOut()
  if err != nil {
    t.Error(err)
  }
  
  if len(out) > 0 {
    t.Errorf(string(out))
  }
  
  err = os.Chdir("../..")
  if err != nil {
    t.Error(err)
  }
}
```

```
```

```
```


