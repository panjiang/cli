# cli

## Init a mysql client (with 'jinzhu/GORM')
`
// Init instance
conf := &db.MysqlConfig{Addr: "localhost:3306", User: "root", Password: "root", DB: "test"}
if err := db.InitMysqlCli(conf); err != nil {
	log.Fatal(err)
}

// Use it 
if err := db.DB.Where("email=?", "test@qq.com").First(&account).Error; err != nil {
	Panic(err)
}

// ...
`
