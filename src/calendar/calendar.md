:: BASE_DOC ::

## API
### Calendar Props

名称 | 类型 | 默认值 | 说明 | 必传
-- | -- | -- | -- | --
confirmBtn | String / Object / Slot / Function | '' | 确认按钮。值为 null 则不显示确认按钮。值类型为字符串，则表示自定义按钮文本，值类型为 Object 则表示透传 Button 组件属性。。TS 类型：`string | TNode | ButtonProps | null`，[Button API Documents](./button?tab=api)。[通用类型定义](https://github.com/Tencent/tdesign-mobile-vue/blob/develop/src/common.ts)。[详细类型定义](https://github.com/Tencent/tdesign-mobile-vue/tree/develop/src/calendar/type.ts) | N
firstDayOfWeek | Number | 0 | 第一天从星期几开始，默认 0 = 周日 | N
format | Function | - | 用于格式化日期的函数。TS 类型：`(day: TDate) => TDate` `type TDateType = 'selected' | 'disabled' | 'start' | 'centre' | 'end' | ''; ` `interface TDate { date: Date; day: number; type: TDateType; className?: string; prefix?: string; suffix?: string; }`。[详细类型定义](https://github.com/Tencent/tdesign-mobile-vue/tree/develop/src/calendar/type.ts) | N
maxDate | Number / Date | - | 最大可选的日期，不传则默认半年后。TS 类型：`number | Date` | N
minDate | Number / Date | - | 最小可选的日期，不传则默认今天。TS 类型：`number | Date` | N
title | String / Slot / Function | - | 标题，不传默认为“请选择日期”。TS 类型：`string | TNode`。[通用类型定义](https://github.com/Tencent/tdesign-mobile-vue/blob/develop/src/common.ts) | N
type | String | 'single' | 日历的选择类型，single = 单选；multiple = 多选; range = 区间选择。可选项：single/multiple/range | N
value | Number / Array / Date | - | 当前选择的日期，不传则默认今天，当 type = multiple 或 range 时传入数组。TS 类型：`number | Date | TCalendarValue[] ` `type TCalendarValue = number | Date`。[详细类型定义](https://github.com/Tencent/tdesign-mobile-vue/tree/develop/src/calendar/type.ts) | N
visible | Boolean | false | 是否显示日历 | N
onConfirm | Function |  | TS 类型：`(value: Date) => void`<br/>点击确认按钮时触发 | N
onSelect | Function |  | TS 类型：`(value: Date) => void`<br/>选择日期时触发 | N

### Calendar Events

名称 | 参数 | 描述
-- | -- | --
confirm | `(value: Date)` | 点击确认按钮时触发
select | `(value: Date)` | 选择日期时触发
