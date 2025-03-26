# ELK

Hệ thống thu thập log và quản lý qua Logstash, Elasticsearch và Kibana

## Note

Logstash nhận dữ liệu qua 2 pipeline và lưu vào 2 indeces, 1 cho các hoạt động của user, 1 cho các hoạt động của hệ thống

Lưu ý khi nhận dữ liệu từ kafka thì chú ý config trong /config/logstash

## Format data

user-logs sẽ nhận dữ liệu định dạng:

```json
{
  username: "quangvu30",
  IP: "192.168.0.1",
  action: "POST",
  useragent: "Mozila",
  url: "/api/v1/order",
  data: any
}
```

system-logs sẽ nhận định dạng string:

`2025-03-25T10:22:35.700Z [error] (rubber-margin): Cannot read properties of null (reading '_id')`

Lưu ý rằng system-logs trong elasticsearch sẽ lưu thành các index theo ngày ví dụ:
`system-logs-2025.03.25`
