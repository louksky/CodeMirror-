# CodeMirror-
code miror implement on simple html
just extarct the file from zip rar lib in the same folder as html page






<html>
    <head>
        <link rel="stylesheet" href="codemirror-5.53.2/lib/codemirror.css">
        <script src="codemirror-5.53.2/lib/codemirror.js"></script>
        <script src="codemirror-5.53.2/mode/javascript/javascript.js"></script>
        <script src="codemirror-5.53.2/mode/python/python.js"></script>
        
        <script src="codemirror-5.53.2/addon/fold/foldcode.js"></script>
        <script src="codemirror-5.53.2/theme/panda-syntax.css"></script>
        <link rel="stylesheet" href="http://codemirror.net/theme/lesser-dark.css">
    </head>
    <body>
        <form style="width:200%; margin-left: 13%; ">
            <textarea id="code" name="code" style="height: 50rem;">


            </textarea>
        </form>

        <script>
            window.onload = function() {
                window.editor = CodeMirror.fromTextArea(code, {
                    mode: "javascript",
                    lineNumbers: true,
                    lineWrapping: true,
                    theme: "lesser-dark",
                    foldGutter: {
                        rangeFinder: new CodeMirror.fold.combine(CodeMirror.fold.brace, CodeMirror.fold.comment)
                    },
                    gutters: ["CodeMirror-linenumbers", "CodeMirror-foldgutter"]
                });
            };
            window.editor.setOption("mode", language);
        </script>
    </body>
</html>
