
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

![avatar][base64str]


[base64str]:data:image/png;base64,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