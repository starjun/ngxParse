
## 使用方法
```
package main
import (
 "fmt"
 "io/ioutil"

 "github.com/starjun/ngxParse/parser"
)

func main() {
 conf, _ := ioutil.ReadFile("./1.conf")
 ups, sers, err := parser.CHJ_ngx_Parser(string(conf))
 if err != nil {
  fmt.Println("解析配置文件失败: ", err)
 }
 parser.Printf_Color(ups)
 fmt.Println("--------------")
 parser.Printf_Color(sers)
 // Ngx_test()
}
```

## 效果

![avatar][https://raw.githubusercontent.com/starjun/ngxParse/master/效果.png]

