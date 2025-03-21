# ELK

Hệ thống sẽ thu thập log từ tất cả các service và quản lý thông qua Logstash, Elasticsearch, Kibana.

## Note

Logstash cấu hình nhận dữ liệu từ 2 pipeline để chia dữ liệu vào 2 indeces, 1 cho các hoạt động của user, 1 cho các hoạt động của hệ thống

Nếu nhận dữ liệu từ kafka chú ý config trong thư mục /logstash/pipeline
