# 绑定信息

---

### 根据园区搜索未绑定设备列表 \(type,status\)

* **Uri:**  
  `/warehose/{warehose_id}/device?type={typeid}&status={status}page_size={page_size}&page={page}`

* **Methon:**  
  ** **`GET`

* **Response**

```js
{
    "code": 200,
    "message": "",
    "data":
    {
        "pagesize":"xxx", //每一页条数
        "page":"xxx",     //页码
        "total":xxxx,     //总计条数
        "data":[
            {
                "warehose_id":"xxxx",          //园区ID
                "device_number":"xxxx",          //设备编号
                "device_type":"1",

            },{...}
        ]
    }
}
```



