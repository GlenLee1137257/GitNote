流水线：移动端收银台

1.里面手动执行可以选择环境的
2.不区分生产生产测试这些的
3.只区分是否在线运行离线包运行，有无小齿轮

m_cashier__prod_official：线上包｜正式包
m_cashier__prod：线上包｜测试包（带小齿轮）
m_cashier__offline：离线包

测试环境部署：
253部署路径：cd /data/webapps/web-h5/h5app/mobile-cashier

生产灰度环境：RD自行部署