# 前言

任何的项目立项前都要确定需求范围和测试范围。需求范围≠测试范围，因为对于已有产品的升级或紧急运维BUG修复，都需要将原有的功能进行全面测试。作为项目管理也有四年，想总结总结认识和看法。对于项目管理经验留痕和不断改进。

# 项目立项前

任何项目在立项前，所有项目成员都要进行统一认识的宣讲。个人经验来看，总是会存在项目组成员都是老熟人或者项目过程中新协调加入的项目组成员是老熟人，而疏忽于项目宣讲，而导致项目研发和测试过程中，大家认识不统一，摩擦不断。所以不能存在侥幸心理。只有先期的麻烦，才能给以后带来便利。

## 始于宣讲

项目都是渐进明细的，所以我们不能过分要求产品经理，对需求说明及原型在编写时，能百分之百覆盖所有情况。故我们除因产品经理对需求有特殊说明，不然我们需要一些通用做法，避免产品说明未覆盖而引起争议。

* **字段长度问题**：
  * 1、富文本或多文字类型：2000字（汉字），数据库设计时要考虑HTML标签+2000。
  * 2、普通类型名称类型：50字（汉字）,基本能覆盖普通名称长度。
* **文字换行或截取**：（为了样式不易变形，通常采取截取模式）
  * 1、表格中：
    * a、人名不能截取，字多换行
    * b、时间如需截取，必须显示到日期
    * c、其它格式最好能通过CSS3样式文本溢出自适应方式，如不能，建议js保留5-10个，已便识别
  * 2、列表
    * a、通过CSS3样式文本溢出，通常截取10个字
* **数字精度**:
  * 1、数据库设计：在数据值不大时，decimal类型存储，因浮点型等数据类型，存储的值都是近视值。但decimal类型会显示定义的小数位无意义的0，显示时需要做处理。
  * 2、单位：任何涉及到单位的数据，都必须注明单位，数据展示多采用元、米、平方米等基本单位

## 需求范围的确定

很多产品经理，不愿画原型，写需求文档，或者原型粗糙和描述简短不清容易歧义。关于这个，最次需要写需求列表，描述清楚细节。对于老项目的修改，要说清连锁需要修改的地方。避免研发,对整个项目认识不全面而修改不到位，而引起新bug。

## 测试范围的确定

前言中说了，需求范围和测试范围不一样。所有测试范围，对于不管任何项目都应该要整体测试。这就带来一个新的问题，不是本次需求范围内的引起BUG问题，如何管理？本次需求引起的缺陷或者原有功能严重性缺陷必须修改，因为不修复会影响客户使用，这个我们不需要纠结，毕竟原有功能新发现严重性缺陷较少。对于原有功能上新发现的BUG，但是又不影响功能，毕竟原有隐藏的问题有多少，未知风险很大（最要是要话大量的时间，而且会不会有连锁反应也未知），这是我们最纠结的，修不修复，容易争执。

我个人有两点建议：一是；立项时对此类问题一律要求归纳至新需求立项修改；二是,立项是对于此类问题流出一定风险时间，对这些问题新发现的问题进行优先级排序，对于超过预期的，归纳至新需求立项修改。

个人建议采用第二种，毕竟老问题新发现难免。故此立项时时间周期一定要估算清楚。

# 项目研发中

# 项目结项









