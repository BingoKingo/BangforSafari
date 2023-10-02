# [DuckDuckGo Bang](https://duckduckgo.com/bangs) for [xSearch](https://apps.apple.com/app/id1579902068) on Safari

Make **DuckDuckGo Bang** available on Safari (iOS. macOS). You need to install the **xSearch** App from App Store and import the [ddgbang.xsearch](./ddgbang.xsearch) file into the xSearch App.

**Note**: The file is large and may not be imported at once or may cause Safari laggy or crashed after importing.

## Detail

The Original JSON File is from <https://duckduckgo.com/bang.js> ([v255](https://duckduckgo.com/bang.v255.js)).

A few steps:
replace `,"r":\d+` with `"r":\d+,`,
replace `,"c":"\w+"` with `"c":"\w+",`,
replace `,"c":"\w+\s\w+"` with `"c":"\w+\s\w+",`,
replace `,"sc":"\w+"` with `"sc":"\w+",`,
replace `,"sc":"\w+\s\w+"` with `"sc":"\w+\s\w+",`,
replace `,"sc":"\w+\s\(\w+\)"` with `"sc":"\w+\s\(\w+\)",`,
replace `,"sc":"\w+\/\w+"` with `"sc":"\w+\/\w+",`,
replace `,"sc":"\w+..\w+.\w+."` with `"sc":"\w+..\w+.\w+.",`,
replace `,"sc":"\w+..\w+..."` with `"sc":"\w+..\w+...",`,
replace `,"sc":"\w+.\w+..\w+."` with `"sc":"\w+.\w+..\w+.",`,
replace `,"sc":"\w+...\w+."` with `"sc":"\w+...\w+.",`,
replace `,"d":"\w+.\w+"` with `"d":"\w+.\w+",`,
replace `,"d":"\w+.\w+.\w+"` with `"d":"\w+.\w+.\w+",`,
replace `,"d":"\w+.\w+.\w+.\w+"` with `"d":"\w+.\w+.\w+.\w+",`,
replace `,"d":"\w+.\w+.\w+.\w+.\w+"` with `"d":"\w+.\w+.\w+.\w+.\w+",`,
replace `,"d":"\w+.\w+.\w+.\w+.\w+.\w+"` with `"d":"\w+.\w+.\w+.\w+.\w+.\w+",`,
replace `,"d":"\w+.\w+.\w+.\w+.\w+.\w+.\w+"` with `"d":"\w+.\w+.\w+.\w+.\w+.\w+.\w+",`,
replace `,"d":"%s.\w+.\w+"` with `"d":"%s.\w+.\w+",`,
replace `,"d":"\w+.%s.\w+.\w+"` with `"d":"\w+.%s.\w+.\w+",`,
replace `,"d":""` with `"d":"",`,
replace`"u":` with `"mobile":`,
replace`"t":` with `"shortcuts":`,
replace`"s":` with `"title":`,
replace`{{{s}}}` with `%s `,
replace `%s ` with `%s`,
delete `{"mobile":"/newbang","shortcuts":"nbang","title":"duckduckgo new !bang"},`,
replace `{"title":"Search all !bangs","mobile":"/bang?q=%s","shortcuts":"bang"},` with `{"title":"Search all !bangs","mobile":"https://ddg.gg/bang?q=%s","shortcuts":"bang"},`,
replace `"mobile":"/` with `"mobile":"https://ddg.gg/`,
replace `http://duckduckgo.com/` with `https://duckduckgo.com/`,
replace `https://duckduckgo.com/` with `https://ddg.gg/`,
replace `{"shortcuts":"/?s","mobile":"https://activehi.com/?s=%s","title":"ActiveHi News"},` with `{"shortcuts":"activehi","mobile":"https://activehi.com/?s=%s","title":"ActiveHi News"},`,
replace `"shortcuts":"(\w+)"` with `"shortcuts":["$1"]`,
replace `"shortcuts":"(\w+.\w+)"` with `"shortcuts":["$1"]`,
replace `"shortcuts":"(\w+.)"` with `"shortcuts":["$1"]`,
replace `"shortcuts":"(.\w+)"` with `"shortcuts":["$1"]`,
replace `"shortcuts":"(.)"` with `"shortcuts":["$1"]`,
replace `"shortcuts":"(..)"` with `"shortcuts":["$1"]`,
replace `"shortcuts": "(\w+.\w+.\w+)"` with `"shortcuts":["$1"]`,
convert unicode to strings,
replace `"shortcuts":"([^\u201c-\u201d]+)"` with `"shortcuts":["$1"]`,
delete invalid strings `"c++ref"`, `"پخشستاره"`, `"موبايل"`, `"מורפיקס"`, `"гбг"`, `"карты"`, `"нпсд"`, `"ასტრო"`,
dedupe,
format,
done.