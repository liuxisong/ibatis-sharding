# 关于Sharding #

在使用数据库处理大量数据的时候，如果考虑成本，不购买处理能力很强的服务器，或者干脆数据量大到单台服务器无法处理的时候，我们经常需要对数据进行切分，常见的切分方式有两种：

## 垂直切分 ##

垂直切分是按系统的功能，将不同的功能的数据放在不同的数据库上，比如\*客户\*数据放到db1上，**订单\*数据放到db2上，等等，这样划分能比较好的对数据库进行优化，比如，客户的数据大部分时间是读取，我们可以针对数据读取进行优化，而订单数据可能经常是做更新，做事务，我们需要对事务进行优化**

很多情况下，我们只需要对数据进行垂直切分就可以满足要求了，但是，如果会员数据量特别大，大到一台服务器无法处理的时候呢？我们就需要对数据进行水平切分了。

## 水平切分 ##

  * TODO 