# wefFFWEFwe

```java
public class Post implements EntryPoint {
    @Override
    public void onModuleLoad() {
        var markedOption = JsPropertyMap.of();
        markedOption.set("gfm", true);
        markedOption.set("tables", true);
        markedOption.set("breaks", false);
        markedOption.set("smartLists", true);
        markedOption.set("langPrefix", "language-");
        BiFunction<String, String, String> highlight = (code, lang)-> {
            DomGlobal.console.log(code + ", " + lang);
            DomGlobal.console.log(Hljs.highlight(lang, code).value);
            return Hljs.highlight(lang, code).value;
        };
        markedOption.set("highlight", highlight);
        DomGlobal.console.log(markedOption);
        Marked.setOptions(markedOption);
        DaggerComponent.create().view().layout();
    }
}

```

https://google.com

ㅈㄷㄹㅈㄷㄹ
ㅈㄷㄹㄷㅈㄹ
ㄹㅈㄷㄹ


| Header 1 | Header 2 | Header 3 |
| ---------|:--------:| ---------|
| Cell 1-1  | Cell 1-2 | Cell 1-3 |
| Cell 2-1  | Cell 2-2 | Cell 2-3 |