# 案例说明

本说明使用事件库的读者序号，与v3.2数据文件对应。以下说明区分来源事实、观察窗口和分析解释。

## 第57案：ESD收缩与锚定修复窗口

本案关注2020年末至2021年初ESD已经低于目标价格后，coupon机制吸引持有人销毁ESD并参与供给收缩的过程。项目AMA和社区方案说明coupon的兑付条件及激励约束，为讨论该窗口的修复机制提供依据；M_PR编码对应该窗口。

这一记录不能据此确定ESD首次脱锚的起因，也不能排除coupon期限、需求和收益设计等竞争解释。首次脱锚原因及不同设计解释之间的因果关系仍未确定。记录中的“首个关键风险条件”应在所述收缩修复窗口内理解，不外推为ESD整个失稳过程的唯一根因。

事件依据：[Empty Set Dollar项目AMA](https://medium.com/emptysetdollar/an-ama-with-equal-parenthesis-a1c29dafc239)。

## 第8案：SVB冲击USDC

本案记录2023年3月10日至15日的储备银行冲击与后续市场变化。Circle披露33亿美元USDC储备位于SVB，银行可用性风险随后影响赎回预期与市场价格。储备受影响、价格偏离和后续风险解除属于不同环节，33亿美元是受影响储备规模，不应当作已实现损失。

本案保留稳定币特有风险标签，分析对象是储备可得性对面值兑付的支撑关系。若以银行冲击在稳定机制中的传播为分析对象，也可从重塑风险解释该过程。单一标签取决于观察粒度，不表示银行风险本身为稳定币独有。

事件依据：[Circle关于储备风险解除与回锚的说明](https://www.circle.com/pressroom/3-3-billion-of-usdc-reserve-risk-removed-dollar-de-peg-closes)。

## 第45案：DEUS Finance预言机操纵

本案事件日期为 **2022年4月28日**。记录涉及DEI价格输入被操纵后的借贷过程，应与2022年3月15日另一次预言机攻击区分。攻击者收益约1,340万美元与安全机构估算的协议影响约1,570万美元采用不同口径，不合并为同一个损失数值。

本案保留重塑风险标签，判断关注价格输入、抵押借贷与DEI发行之间的机制联系。DEUS官方审计版本中，`DeiLenderSolidex.borrow`经过依赖预言机价格的偿付检查后，调用`MintHelper.mint`，后者调用`DEI.pool_mint`；同一辅助合约还连接虚拟储备和全局抵押率。这些代码为借贷与稳定币发行的联系提供依据。该审计版本未在本次说明中与攻击时部署字节码比对，代码证据不等同于攻击交易重放。

机制依据：[DeiLenderSolidex.borrow](https://github.com/deusfinance/lending-audit/blob/6051a63ffd0a5d154d957794a88df72cc9d2e4bc/contracts/DeiLenderSolidex.sol#L257)及[MintHelper](https://github.com/deusfinance/lending-audit/blob/6051a63ffd0a5d154d957794a88df72cc9d2e4bc/contracts/MintHelper.sol#L54)。

事件依据：[CertiK借贷协议年度回顾](https://www.certik.com/blog/2022-year-in-review-lending-protocols)；补充来源：[DEUS DAO第二次攻击分析](https://rekt.news/deus-dao-rekt-2)。

## 第88案：Garantex与USDT冻结

本案将被指违法金融活动的持续区间与2025年3月执法、平台处置及稳定币冻结区分记录。USDT在交易平台中的兑换用途、发行人冻结能力及联合执法涉及的多资产规模属于不同事实。冻结金额不等于平台全部违法交易金额，也不等于稳定币发行人的资产损失。

v3.2将本案编码为继承风险。去除稳定价值目标后，交易平台提供违法资金服务的风险仍然成立；现有记录不足以仅凭使用USDT确定风险机制已被稳定机制重塑。主要风险起点仍为外部生态中的违法利用。

事件依据：[Tether关于协助冻结约2,300万美元的说明](https://tether.io/news/tether-recognized-for-assisting-the-united-states-secret-service-in-23m-freeze-related-to-transfers-on-sanctioned-exchange-garantex/)。

## 第102案：Paxos停止新增发行BUSD

本案对象为Paxos发行的BUSD，与Binance-Peg BUSD区分。停止新增发行于2023年2月13日宣布，2月21日生效。停止铸造、持续赎回和供应收缩分别记录；已完成赎回金额表示兑付规模，不表示资产损失。

v3.2将本案编码为重塑风险。NYDFS指出，停发源于Paxos监督其与Binance合作关系的未解决问题。监管限制也适用于一般加密资产；在本案中，稳定币的发行与赎回安排将该限制传导为停止新增发行、持续兑付和供应收缩。主要风险起点仍为外部生态中的监管法域。

事件依据：[NYDFS通知](https://www.dfs.ny.gov/consumers/alerts/Paxos_and_Binance)；[Paxos停止铸造BUSD的公告](https://www.paxos.com/newsroom/paxos-will-halt-minting-new-busd-tokens)。

## 第103案：Tether旧链停止支持

本案记录旧链支持退出计划及其后续更新。现有公告将相关安排解释为业务和基础设施调整，尚不足以确认具体监管因素。v3.2沿用既有监管法域与特有风险编码，作为待复核标签；相应分类计数包含该案，不应将其理解为监管原因已经证实。

事件依据：[Tether基础设施评估及旧链退出公告](https://tether.io/news/tether-to-wind-down-usdt-support-for-five-legacy-blockchains-as-part-of-strategic-infrastructure-review/)。

## 正文中的额外文献例证

Curve 3Pool中的USDT流动性失衡、Terra崩溃期间USDT承压用于正文的机制讨论，属于额外文献例证，不计入本发布包的108案，也不增加相应分类计数。
