
## Run elasticsearch

```bash
$ d run --name elasticsearch -p 9200:9200 -d -v "$PWD/config":/usr/share/elasticsearch/config -v "$PWD/data":/usr/share/elasticsearch/data anson2048/elasticsearch:0.0.1 
```

## Run kibana

```bash
$ d run --name kibana --link elasticsearch:elasticsearch -p 5601:5601 -d anson2048/kibana:0.0.1 --plugins elasticsearch/marvel/latest
```



## 参考

- [kibana 中文文档](https://www.gitbook.com/book/chenryn/kibana-guide-cn)
- [ELKstack 中文指南](https://www.gitbook.com/book/chenryn/kibana-guide-cn)