
calendar-converter
==================

公农历互转组件（ date converter between solar and lunar ）

###使用示例（Example）:###

---

        var cc  =new CalendarConverter;

        cc.lunar2solar(new Date(2011, 0, 3)); ---> 2010,11,29
        cc.solar2lunar(new Date(2010, 10, 29)); ----> 2011, 1, 3

        农历转公历时，如果那一月是那一年的闰月，则需额外传一个参数，才能得到正确的公历日期
        cc.solar2lunar(new Date(2012, 4, 27)); ---> 2012年4月初7, 其中 isLeap为true，表示为闰四月
        cc.lunar2solar(new Date(2012, 3, 7)) ---> 得到错误时间：2012, 4, 27
        cc.lunar2solar(new Date(2012, 3, 7), true) --> 正确: 2012, 5, 27

        result:
         {
           cDay: "戊戌"
            , cMonth: "丁未"
            , cYear: "壬辰"
            , isLeap: false             // 该月是否为闰月
            , lDay: 18
            , lMonth: 6
            , lYear: 2012
            , lunarDay: "十八"
            , lunarFestival: ""
            , lunarMonth: "六"
            , lunarYear: "龙"
            , sDay: 5
            , sMonth: 8
            , sYear: 2012
            , solarFestival: ""         // 节日
            , solarTerms: ""            // 节气
            , week: "日"                // 周几
         }
###联系方式（Contact）:###

---
 - StuPig Gong <shouqiang.gong@gmail.com>