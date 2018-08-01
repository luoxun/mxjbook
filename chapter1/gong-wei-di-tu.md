# 工位地图

---

### 根据园区信息返回工位地图

* **Uri:**  
  `/station/warehose/{warehose_id}/layer/`

* **Methon:**  
  ** **`GET`

* **Response**

```js
{
    "code": 200,
    "message": "",
    "details": null,
    "data": [{
            "warehose_id":"xxxx",          //园区ID
            "station_id":"xxxx",          //工位ID
            "station_type":"xxxx",        //工位类型
            "station_status":"1",         // 1 可以预定 2.已经预定 3,使用中   
        },{...}],
}
```

### 上传工位地图

* **Uri:**  
  `/station/warehose/{warehose_id}/map/upload`

* **Methon:**  
  ** **`POST` {application/x-www-form-urlencoded}

* **Request**

  ```js
  {
    "file":@file             //上传图片
  }
  ```

* **Response**

```js
{
    "code": 200,
    "message": "",
    "data": "https://xxxxxxx/img.png" //图片地址
}
```



