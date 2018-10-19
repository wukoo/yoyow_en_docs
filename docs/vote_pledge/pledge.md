# 抵押

每期矿工见证人的名额，根据各见证人抵押进行选择。

## 抵押排名规则

- 基本思路为根据各账号有效抵押安排排名。如：只有ABC三人抵押，其中A有效抵押6个币，B有效抵押3个币，C有效抵押1个币，那么在后续100个块中，应该安排A出块60个，B出块30个，C出块10个。
- 有效抵押为'7天内平均抵押'与'当前抵押'两者较小值。
- 即：增加抵押时，有效抵押数缓慢增加；降低或解除抵押时，有效抵押立即减少。

## 抵押的提取
降低抵押金额或者解除抵押时，押金延迟一段时间后退还，当前设置为1天。
注：1） 连续多次降低抵押时，金额累加一起退还，计划退还时间以最后一次降低时间为准进行延迟
    2）增加抵押时，如果当前账号有延迟退还的押金，优先从里面扣，不足部分从余额扣取