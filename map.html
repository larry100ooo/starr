<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Maps 批量截圖工具</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background: #f5f5f5;
        }
        .container {
            background: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #1a73e8;
            text-align: center;
            margin-bottom: 30px;
        }
        .input-section {
            margin-bottom: 30px;
        }
        textarea {
            width: 100%;
            height: 200px;
            padding: 15px;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-family: monospace;
            font-size: 14px;
            resize: vertical;
        }
        .button-group {
            text-align: center;
            margin: 20px 0;
        }
        button {
            background: #1a73e8;
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin: 0 10px;
        }
        button:hover {
            background: #1557b0;
        }
        button:disabled {
            background: #ccc;
            cursor: not-allowed;
        }
        .results {
            margin-top: 30px;
        }
        .address-item {
            background: #f8f9fa;
            border: 1px solid #e0e0e0;
            border-radius: 5px;
            padding: 15px;
            margin-bottom: 15px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .address-info {
            flex: 1;
        }
        .address-title {
            font-weight: bold;
            color: #333;
            margin-bottom: 5px;
        }
        .address-detail {
            color: #666;
            font-size: 14px;
        }
        .map-link {
            background: #34a853;
            color: white;
            padding: 8px 15px;
            border-radius: 5px;
            text-decoration: none;
            margin-left: 10px;
        }
        .map-link:hover {
            background: #2d8f47;
        }
        .instructions {
            background: #e8f4fd;
            padding: 20px;
            border-radius: 5px;
            margin-bottom: 30px;
        }
        .instructions h3 {
            color: #1a73e8;
            margin-top: 0;
        }
        .instructions ol {
            margin: 10px 0;
        }
        .instructions li {
            margin: 5px 0;
        }
        .warning {
            background: #fff3cd;
            border: 1px solid #ffeaa7;
            padding: 15px;
            border-radius: 5px;
            margin-bottom: 20px;
        }
        .warning h4 {
            color: #856404;
            margin-top: 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🗺️ Google Maps 批量截圖工具</h1>
        
        <div class="warning">
            <h4>⚠️ 使用說明</h4>
            <p>此工具會為您的地址生成Google Maps連結，您可以使用瀏覽器擴充功能或自動化工具進行批量截圖。請確保遵守Google Maps的使用條款。</p>
        </div>

        <div class="instructions">
            <h3>📋 使用步驟</h3>
            <ol>
                <li>點擊「載入地址資料」按鈕，系統會自動載入您的連江縣地址清單</li>
                <li>或手動輸入地址（每行一個，格式：編號|縣市|鄉鎮|地址）</li>
                <li>點擊「生成地圖連結」</li>
                <li>點擊各個「開啟地圖」按鈕，在新分頁中開啟Google Maps</li>
                <li>使用瀏覽器截圖工具或擴充功能進行批量截圖</li>
            </ol>
        </div>

        <div class="input-section">
            <h3>地址資料輸入</h3>
            <textarea id="addressInput" placeholder="格式：編號|縣市|鄉鎮市區|地址&#10;例如：2|連江縣|北竿鄉|中山路174號"></textarea>
            <div class="button-group">
                <button onclick="loadDefaultData()">載入地址資料</button>
                <button onclick="generateLinks()">生成地圖連結</button>
                <button onclick="clearData()">清除資料</button>
            </div>
        </div>

        <div class="results" id="results"></div>
    </div>

    <script>
        const defaultAddresses = [
            "2|連江縣|北竿鄉|中山路174號",
            "3|連江縣|北竿鄉|中山路180號",
            "4|連江縣|北竿鄉|中山路192號",
            "5|連江縣|北竿鄉|中山路194號",
            "7|連江縣|北竿鄉|中山路196號",
            "8|連江縣|北竿鄉|中山路198號",
            "12|連江縣|北竿鄉|中山路219號",
            "13|連江縣|北竿鄉|中山路221號",
            "14|連江縣|北竿鄉|中山路224號",
            "19|連江縣|北竿鄉|273號",
            "20|連江縣|北竿鄉|塘岐村231號",
            "21|連江縣|南竿鄉|清水村98號",
            "22|連江縣|南竿鄉|清水村117號",
            "23|連江縣|南竿鄉|清水村116號",
            "25|連江縣|南竿鄉|清水村104號",
            "26|連江縣|南竿鄉|福沃村63號",
            "27|連江縣|南竿鄉|福沃村57號",
            "30|連江縣|南竿鄉|馬祖村8號",
            "31|連江縣|南竿鄉|馬祖村11號",
            "32|連江縣|南竿鄉|馬祖村97號",
            "35|連江縣|南竿鄉|馬祖村87號",
            "36|連江縣|南竿鄉|馬祖村83號",
            "37|連江縣|南竿鄉|馬祖村79號",
            "38|連江縣|南竿鄉|馬祖村77號",
            "39|連江縣|南竿鄉|馬祖村75號",
            "40|連江縣|南竿鄉|馬祖村73號",
            "41|連江縣|南竿鄉|馬祖村67號",
            "42|連江縣|南竿鄉|馬祖村59號",
            "46|連江縣|南竿鄉|馬祖村100號",
            "49|連江縣|南竿鄉|馬祖村80號",
            "50|連江縣|南竿鄉|馬祖村74號",
            "51|連江縣|南竿鄉|馬祖村62號",
            "52|連江縣|南竿鄉|馬祖村64號",
            "56|連江縣|南竿鄉|清水村161",
            "57|連江縣|南竿鄉|清水村100",
            "59|連江縣|南竿鄉|清水村126-5",
            "60|連江縣|南竿鄉|清水村126-3",
            "61|連江縣|南竿鄉|清水村126-4",
            "65|連江縣|南竿鄉|清水路117-3號",
            "72|連江縣|南竿鄉|福沃村98號",
            "73|連江縣|南竿鄉|福沃村110號",
            "74|連江縣|南竿鄉|福沃村110-1號",
            "75|連江縣|南竿鄉|介壽村228號",
            "76|連江縣|南竿鄉|介壽村231號",
            "78|連江縣|南竿鄉|介壽村216號",
            "79|連江縣|南竿鄉|介壽村218號",
            "81|連江縣|南竿鄉|介壽村52號",
            "85|連江縣|南竿鄉|復興村220號"
        ];

        function loadDefaultData() {
            document.getElementById('addressInput').value = defaultAddresses.join('\n');
        }

        function generateLinks() {
            const input = document.getElementById('addressInput').value.trim();
            if (!input) {
                alert('請先輸入地址資料');
                return;
            }

            const lines = input.split('\n').filter(line => line.trim());
            const results = document.getElementById('results');
            results.innerHTML = '<h3>🔗 生成的地圖連結</h3>';

            lines.forEach((line, index) => {
                const parts = line.split('|');
                if (parts.length >= 4) {
                    const [id, county, district, address] = parts;
                    const fullAddress = `${county}${district}${address}`;
                    const encodedAddress = encodeURIComponent(fullAddress);
                    const mapUrl = `https://www.google.com/maps/search/${encodedAddress}`;
                    
                    const addressItem = document.createElement('div');
                    addressItem.className = 'address-item';
                    addressItem.innerHTML = `
                        <div class="address-info">
                            <div class="address-title">編號 ${id}</div>
                            <div class="address-detail">${fullAddress}</div>
                        </div>
                        <a href="${mapUrl}" target="_blank" class="map-link">開啟地圖</a>
                    `;
                    results.appendChild(addressItem);
                }
            });

            // 添加批量開啟功能
            const batchButton = document.createElement('button');
            batchButton.textContent = '批量開啟所有地圖 (⚠️ 會開啟很多分頁)';
            batchButton.style.marginTop = '20px';
            batchButton.style.backgroundColor = '#ea4335';
            batchButton.onclick = function() {
                if (confirm('這將會開啟 ' + lines.length + ' 個新分頁，確定要繼續嗎？')) {
                    lines.forEach((line, index) => {
                        const parts = line.split('|');
                        if (parts.length >= 4) {
                            const [id, county, district, address] = parts;
                            const fullAddress = `${county}${district}${address}`;
                            const encodedAddress = encodeURIComponent(fullAddress);
                            const mapUrl = `https://www.google.com/maps/search/${encodedAddress}`;
                            
                            // 延遲開啟避免瀏覽器阻擋
                            setTimeout(() => {
                                window.open(mapUrl, '_blank');
                            }, index * 500);
                        }
                    });
                }
            };
            results.appendChild(batchButton);
        }

        function clearData() {
            document.getElementById('addressInput').value = '';
            document.getElementById('results').innerHTML = '';
        }

        // 頁面載入時自動載入資料
        window.onload = function() {
            loadDefaultData();
        };
    </script>
</body>
</html>