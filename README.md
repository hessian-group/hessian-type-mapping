# hessian cross languages type mapping 

Cross languages message definition should be careful, the following situations should be avoided:
- define object that only exists in a special language
	- using various java exceptions (using error code/message instead)


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
| **OTHER COMMON USING TYPE** | | | 
| **big decimal** | java.math.BigDecimal | github.com/dubbogo/gost/math/big/Decimal |
| **Boolean** | Boolean | \*bool (TODO) |
| **Integer** | Integer | \*int (TODO)|
| **Long** | Long | \*int64 (TODO)|
| **Double** | Double | \*float64 (TODO) |

## reference

- [hessian serialization](http://hessian.caucho.com/doc/hessian-serialization.html)

