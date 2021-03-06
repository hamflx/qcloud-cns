# 腾讯云云解析SDK

[![GoDoc](https://godoc.org/github.com/athurg/go-qcloud-cns-sdk?status.svg)](http://godoc.org/github.com/athurg/go-qcloud-cns-sdk)

[腾讯云 云解析模块API](https://cloud.tencent.com/document/product/302) Go语言SDK

## 使用方法
```sh
go get github.com/athurg/go-qcloud-cns-sdk 
```

## 使用范例
```golang
package main

import (
	"github.com/athurg/go-qcloud-cns-sdk"
	"log"
)

func main() {
	cli := cns.New("secretId", "secretKey")
	domains, err := cli.DomainList()
	if err != nil {
		log.Fatal(err)
	}

	for _, domain := range domains {
		log.Println(domain)
	}
}
```


## 完成状态

- [x] 域名相关接口
- - [x] 添加域名
- - [x] 设置域名状态
- - [x] 获取域名列表
- - [x] 删除域名
- [x] 解析记录相关接口
- - [x] 添加解析记录
- - [x] 设置解析记录状态
- - [x] 修改解析记录
- - [x] 获取解析记录列表
- - [x] 删除解析记录
