# config

## support

support files with extension: json, toml, yaml, yml, properties, props, prop, hcl.

## usage

`govendor fetch github.com/xwi88/config`

## example

```go
	type redisOptions struct {
		Host        string
		Port        string
		Password    string
		IdleTimeout int
		MaxIdle     int
		MaxActive   int
	}

	type testConf struct {
		Name  string
		Redis redisOptions
	}

	var conf testConf

	testfile := "./testdata/app_test.toml"
	err := LoadConfig(testfile, &conf)
	if err != nil {
		// some deal
    }
    
    fmt.Println(conf.Host)
```
