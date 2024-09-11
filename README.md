<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>オプションボタンの選択</title>
</head>
<body>
    <form id="myForm">
        <p>好きなフルーツを選んでください:</p>
        <input type="radio" id="apple" name="fruit" value="Apple">
        <label for="apple">Apple</label><br>
        <input type="radio" id="banana" name="fruit" value="Banana">
        <label for="banana">Banana</label><br>
        <input type="radio" id="cherry" name="fruit" value="Cherry">
        <label for="cherry">Cherry</label><br><br>
        <button type="button" onclick="showSelected()">表示</button>
    </form>

    <script>
        function showSelected() {
            // 選択されているオプションを取得
            const selectedFruit = document.querySelector('input[name="fruit"]:checked');
            if (selectedFruit) {
                // 選ばれた項目をアラートで表示
                alert("選んだフルーツは: " + selectedFruit.value);
            } else {
                // 何も選ばれていない場合の処理
                alert("何も選ばれていません。");
            }
        }
    </script>
</body>
</html>
