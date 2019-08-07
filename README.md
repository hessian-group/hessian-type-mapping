# hessian cross language type mapping 

cross language message definition should be careful, the following situations should be avoid:
- define object that only exists in a special language
	- not using various java exceptions, using error code/message instead.
	- not using packaging type Integer,Long,Boolean in java, using raw type instead.


So we maintain a cross language type mapping:

| hessian type |  java type  |  golang type | 
| --- | --- | --- | 
| **null** | null | nil | 
| **binary** | byte[] | []byte | 
| **boolean** | boolean | bool |
| **date** | java.util.Date | time.Time |
| **double** | double | float64 |
| **int** | int | int |
| **long** | long | long |
| **string** | java.lang.String | string |
| **list** | java.util.List | slice |
| **map** | java.util.Map | map |
| **object** | custom define object | custom define struct|
| **THE FOLLOWING IS OTHER COMMON USING DATA TYPE** | 
| **big decimal** | java.math.BigDecimal | github.com/dubbogo/gost/math/big/Decimal


## reference

- [hessian serialization](http://hessian.caucho.com/doc/hessian-serialization.html)

