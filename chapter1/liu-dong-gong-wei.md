# 流动工位

---

### page获取流动工位数据

* **Uri:**  
  `/warehose/{warehose_id}/station?page_size={page_size}&page={page}&station_type={station_type}`

* **Methon:**  
  ** **`GET`

* **Response**

```js
{
    "code": 200,
    "message": "",
    "data":
    {
        "page_size":"xxx", //每一页条数
        "page":"xxx",     //页码
        "total":xxxx,     //总计条数
        "data":[
            {
                "group_id":"xxxxxxx",          //工位组ID 全局唯一ID
                "warehose_id":"xxxx",          //园区ID
                "group_name":"xxxx",          //工位组名称
                'group_status':"1",            //工位状态 0为未预定,1为已预定,2为s会用中.
                "user_id":"xxxxx",             //使用人ID
                "user_mobile":"xxxx",         // 使用人电话
                "user_name":""xxxx,          //使用人姓名
                "has_add_number":"xxx",      //已添加工位数
            },{...}
        ]
    }
}
```

### 编辑流动工位

* **Uri:**  
  `/station/warehouse/{warehouseid}/layer/{layerid}/`

* **Methon:**  
  ** **`PUT`

* **Request**
  ```js
  {
    'station_id':'xxxx', //工位编号
    'station_type':'xxxx', //工位类型
    'station_number':'xxxx', //工位号
    'station_group':'xxxxx', //工位组
    'bind_device':'xxxx', // 绑定设置
    'is_bindmap':'xxx' //绑定后工位地图
    'map_longitude':'34' //工位经度
    'map_latitude':'193.3' //工位 纬度
  }
  ```
* **Response**
  ```js
  {
  "code": 200,
  "message": "",
  "data": {
    'station_id':'xxxx', //工位编号
    'station_type':'xxxx', //工位类型
    'station_number':'xxxx', //工位号
    'station_group':'xxxxx', //工位组
    'bind_device':'xxxx', // 绑定设置
    'is_bindmap':'xxx' //绑定后工位地图
    'map_longitude':'34' //工位经度
    'map_latitude':'193.3' //工位 纬度
  }
  ```

### 流动预定办公

* **Uri**  
  `/station/warehose/{warehose_id}/bookings`

* **Methon:**  
  ** **`POST`

* **Request**
  ```js
  {
    "station_id":"xxxx",
    "booking_user":"xxxx",
    "booking_begin":"2018-07-30T09:33:57.650Z",
    "booking_end":"2018-07-30T09:33:57.650Z",
    "booking_type" :1, //1为个人预定,2为管理员预定
    "remark":"remark"
  }
  ```
* **Response**
  ```js
  {
  "code": 200,
  "message": "",
  "data": {
    "bookingid":xxxx,
  }
  ```

### update预定办公

* **Uri**  
  `/station/{station_id}/bookings/{bookingid}`

* **Methon:**  
  ** **`PUT`

* **Request**
  ```js
  {
  "bookinguser":"xxxx",
  "bookingbeging":"2018-07-30T09:33:57.650Z",
  "bookingend":"2018-07-30T09:33:57.650Z",
  "bookingtype" :1, //1为个人预定,2为管理员预定
  "remark":"remark"
  }
  ```
* **Response**
  ```js
  {
  "code": 200,
  "message": "",
  "data": {
    "bookingid":xxxx,
  }
  ```

### 根据流动工位ID获取预约历史 \(需要分页\)

* **Uri:**  
  `/station/{station_id}/bookings/`

* **Methon:**  
  ** **`GET`

* **Response**

  ```js
  {
  "code": 200,
  "message": "",
  "data": {
    "page_size":"xxx", //每一页条数
    "page":"xxx", //页码
    "total":xxxx, //总计条数
    "data":[{
        "booking_id":"xxxxx",
        "booking_begin":'xxxx',
        "booking_end":'xxxxx',
        "booking_type":1,
        "booking_status":1 ,//1为未消费,2为已消费.
        "warehouse" : 'xxx'  
    },{...}
    ]
  }
  ```

  ### 删除流动工位

* **Uri:**
  `/station/station_id/{station_id}/`
* **Methon:**
  ** **`DEL`

* **Response**
  ```js
  {
  "code": 200,
  "message": "",
  "details": null,
  "data": true, //删除成功
  }
  ```



