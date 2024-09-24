# Docx to Json (Input for Abstact of Test command & Pass Criteria Module)

以下是我其他專案為將 Test Plan 轉成  json 的轉換工具中寫的說明文件.md

## 文件說明
* **main.ipynb**
主要程式運行檔案

* **requirements.txt**
運行所需套件，若要使用請輸入：
pip install -r ./requirements.txt
用於載入所有所需套件

* **other docx**
所有待轉換文檔

## 程式碼運行
### 初步萃取
<div>
點擊 main.py ，修改欲萃取的文檔檔名
<pre>
file_name = "{文檔檔名}"
file_abstract(file_name)
# convert_to_dataset(file_name)
</pre>
<span style="color:red;">注意！</span> 此時 "convert_to_dataset(file_name)" 應註解

輸入 <code>Python main.py</code> 來萃取檔案
<br><br>
此時應可看見出現新的檔案
<pre>
{文檔名稱}
    |---- datas.json
    |---- docx.xml
    |---- styles.xml
    |---- output.txt
</pre>
    <li>datas.json : 存放經由 docx.xml 擷取出來的 Test Items</li>
    <li>docx.xml : 存放 docx 主要內容的文件</li>
    <li>styles.xml : docx 中的自定義樣式文件</li>
    <li>output.txt : 純文字的擷取結果</li>
</div>

### 手動標註
<div>
點擊 datas.json 可看見以下資料結構：
<pre>
[
    {
        "test_station": "Test Items Command-BB station",
        "test_item": "Check CV2X FW Version",
        "commandAndCriteria": "...",
        "target": {
            "commands": [],
            "criterias": []
        }
    }
]
</pre>

<br>
請找出 "commandAndCriteria" 欄位中，實際的 command 與 criteria 並記錄在 "commands" & "criterias" 欄位中，像是這樣：
<pre>
[
    {
        "test_station": "Test Items Command-BB station",
        "test_item": "Check CV2X FW Version",
        "commandAndCriteria": "...",
        "target": {
            "commands": [
                "&lt;color value = '#0070C0;&gt;get_cv2x_ver.sh&lt;/color&gt;"
            ],
            "criterias": [
                "&lt;color value = '#FF0000;'>5.16.3&lt;/color&gt;"
            ]
        }
    }
]
</pre>

<br>
點擊 main.py ，將 "file_abstract(file_name)" 註解，並解除註解 "# convert_to_dataset(file_name)
"
<pre>
file_name = "{文檔檔名}"
# file_abstract(file_name)
convert_to_dataset(file_name)
</pre>

<br>
然後輸入 <code>Python main.py</code> 來抓取此檔案的文字位置
最後輸出 "{文檔名稱}/datasets.json"

</div>
<img src="https://scontent.fkhh1-1.fna.fbcdn.net/v/t39.30808-6/345191755_656432502961940_1909636103084342204_n.jpg?_nc_cat=103&ccb=1-7&_nc_sid=6ee11a&_nc_ohc=HcfY8njQQUYQ7kNvgEsBLlV&_nc_ht=scontent.fkhh1-1.fna&oh=00_AYBvbtwDXlOJlTT-fuJILrG03iDPnNc2TIH0p4eOf4H9jQ&oe=66F84359">
