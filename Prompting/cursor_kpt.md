# KPT 회고 단계 안내
_Exported on 12/19/2025 at 09:16:23 GMT+9 from Cursor (2.1.50)_

---

**User**

@Retrospective KPT 회고 (Keep, Problem, Try)를 활용해서 회고 단계를 진행하려고 하는데, 어떻게 해야 하는지 알려줘.

---

**Cursor**


프로젝트 구조 확인 중. KPT 회고 템플릿과 도구를 준비하겠습니다.



KPT 회고 템플릿과 간단한 웹 도구를 준비 중입니다.


```markdown
# KPT 회고 (Keep, Problem, Try)

KPT 회고는 프로젝트나 스프린트 후 개선점을 찾기 위한 간단하고 효과적인 회고 방법론입니다.

## KPT 회고란?

KPT 회고는 세 가지 카테고리로 나누어 회고를 진행합니다:

- **Keep (유지)**: 잘 되고 있어서 계속 유지할 것들
- **Problem (문제)**: 문제가 되었거나 개선이 필요한 것들
- **Try (시도)**: 다음에 시도해볼 것들

## 사용 방법

### 1. 마크다운 템플릿 사용
`template.md` 파일을 열어서 각 섹션에 내용을 작성하세요.

### 2. 웹 도구 사용
`index.html` 파일을 브라우저에서 열어서 인터랙티브하게 회고를 진행할 수 있습니다.

## 회고 진행 단계

1. **Keep 작성**: 이번 기간 동안 잘 되었던 것들을 나열
2. **Problem 작성**: 문제가 되었거나 개선이 필요한 점들을 나열
3. **Try 작성**: Problem에서 도출된 개선 사항들을 구체적인 액션 아이템으로 작성
4. **우선순위 설정**: Try 항목들에 우선순위를 부여
5. **다음 회고에서 검토**: 이전 회고의 Try 항목들이 실제로 시도되었는지 확인

## 팁

- 구체적이고 실행 가능한 항목을 작성하세요
- Problem과 Try를 연결하여 문제 해결 방안을 명확히 하세요
- 팀 회고의 경우 모든 팀원이 참여하도록 하세요
- 정기적으로 회고를 진행하여 지속적인 개선을 추구하세요

```

```markdown
# KPT 회고

**회고 일자**: YYYY-MM-DD  
**회고 기간**: YYYY-MM-DD ~ YYYY-MM-DD  
**참여자**: 

---

## Keep (유지할 것)

이번 기간 동안 잘 되었고 계속 유지해야 할 것들:

- 
- 
- 

---

## Problem (문제점)

이번 기간 동안 문제가 되었거나 개선이 필요한 것들:

- 
- 
- 

---

## Try (시도할 것)

다음 기간에 시도해볼 것들 (Problem에서 도출된 개선 사항):

- 
- 
- 

---

## 액션 아이템

| 우선순위 | Try 항목 | 담당자 | 마감일 | 상태 |
|---------|---------|--------|--------|------|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

---

## 메모

추가로 기록하고 싶은 내용:

```

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>KPT 회고 도구</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            padding: 40px;
        }

        h1 {
            color: #333;
            text-align: center;
            margin-bottom: 10px;
            font-size: 2.5em;
        }

        .subtitle {
            text-align: center;
            color: #666;
            margin-bottom: 40px;
            font-size: 1.1em;
        }

        .header-info {
            display: flex;
            gap: 20px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .header-info input {
            flex: 1;
            min-width: 200px;
            padding: 12px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-size: 14px;
            transition: border-color 0.3s;
        }

        .header-info input:focus {
            outline: none;
            border-color: #667eea;
        }

        .sections {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-bottom: 30px;
        }

        .section {
            background: #f8f9fa;
            border-radius: 12px;
            padding: 25px;
            border: 2px solid transparent;
            transition: all 0.3s;
        }

        .section:hover {
            border-color: #667eea;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.2);
        }

        .section.keep {
            border-left: 5px solid #4caf50;
        }

        .section.problem {
            border-left: 5px solid #f44336;
        }

        .section.try {
            border-left: 5px solid #2196f3;
        }

        .section h2 {
            color: #333;
            margin-bottom: 15px;
            font-size: 1.5em;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .section.keep h2::before {
            content: "✓";
            color: #4caf50;
            font-size: 1.2em;
        }

        .section.problem h2::before {
            content: "⚠";
            color: #f44336;
            font-size: 1.2em;
        }

        .section.try h2::before {
            content: "→";
            color: #2196f3;
            font-size: 1.2em;
        }

        .item-list {
            min-height: 200px;
        }

        .item {
            background: white;
            padding: 12px;
            margin-bottom: 10px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 10px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.05);
        }

        .item input {
            flex: 1;
            border: none;
            padding: 8px;
            font-size: 14px;
            background: transparent;
        }

        .item input:focus {
            outline: none;
            background: #f0f0f0;
            border-radius: 4px;
        }

        .add-item-btn {
            background: #667eea;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            margin-top: 10px;
            transition: background 0.3s;
            width: 100%;
        }

        .add-item-btn:hover {
            background: #5568d3;
        }

        .delete-btn {
            background: #f44336;
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 12px;
            transition: background 0.3s;
        }

        .delete-btn:hover {
            background: #d32f2f;
        }

        .actions {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin-top: 30px;
            flex-wrap: wrap;
        }

        .btn {
            padding: 15px 30px;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
        }

        .btn-primary {
            background: #667eea;
            color: white;
        }

        .btn-primary:hover {
            background: #5568d3;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.3);
        }

        .btn-secondary {
            background: #6c757d;
            color: white;
        }

        .btn-secondary:hover {
            background: #5a6268;
        }

        .export-section {
            margin-top: 30px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 12px;
        }

        textarea {
            width: 100%;
            min-height: 200px;
            padding: 15px;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            resize: vertical;
        }

        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>KPT 회고</h1>
        <p class="subtitle">Keep, Problem, Try 회고 도구</p>

        <div class="header-info">
            <input type="date" id="date" placeholder="회고 일자">
            <input type="text" id="period" placeholder="회고 기간 (예: 2024-01-01 ~ 2024-01-31)">
            <input type="text" id="participants" placeholder="참여자">
        </div>

        <div class="sections">
            <div class="section keep">
                <h2>Keep (유지할 것)</h2>
                <div class="item-list" id="keep-list"></div>
                <button class="add-item-btn" onclick="addItem('keep')">+ 항목 추가</button>
            </div>

            <div class="section problem">
                <h2>Problem (문제점)</h2>
                <div class="item-list" id="problem-list"></div>
                <button class="add-item-btn" onclick="addItem('problem')">+ 항목 추가</button>
            </div>

            <div class="section try">
                <h2>Try (시도할 것)</h2>
                <div class="item-list" id="try-list"></div>
                <button class="add-item-btn" onclick="addItem('try')">+ 항목 추가</button>
            </div>
        </div>

        <div class="actions">
            <button class="btn btn-primary" onclick="exportMarkdown()">마크다운으로 내보내기</button>
            <button class="btn btn-secondary" onclick="loadFromLocalStorage()">저장된 내용 불러오기</button>
            <button class="btn btn-secondary" onclick="saveToLocalStorage()">내용 저장하기</button>
            <button class="btn btn-secondary" onclick="clearAll()">모두 지우기</button>
        </div>

        <div class="export-section hidden" id="export-section">
            <h3>내보낸 마크다운</h3>
            <textarea id="export-text" readonly></textarea>
            <button class="btn btn-primary" onclick="copyToClipboard()" style="margin-top: 10px;">클립보드에 복사</button>
        </div>
    </div>

    <script>
        let itemCounters = { keep: 0, problem: 0, try: 0 };

        function addItem(type) {
            const list = document.getElementById(`${type}-list`);
            const counter = ++itemCounters[type];
            const item = document.createElement('div');
            item.className = 'item';
            item.id = `${type}-item-${counter}`;
            item.innerHTML = `
                <input type="text" placeholder="항목을 입력하세요..." 
                       onchange="saveToLocalStorage()" 
                       id="${type}-input-${counter}">
                <button class="delete-btn" onclick="removeItem('${type}-item-${counter}')">삭제</button>
            `;
            list.appendChild(item);
            item.querySelector('input').focus();
        }

        function removeItem(itemId) {
            document.getElementById(itemId).remove();
            saveToLocalStorage();
        }

        function getAllItems(type) {
            const list = document.getElementById(`${type}-list`);
            const items = list.querySelectorAll('.item input');
            return Array.from(items)
                .map(input => input.value.trim())
                .filter(value => value.length > 0);
        }

        function exportMarkdown() {
            const date = document.getElementById('date').value || new Date().toISOString().split('T')[0];
            const period = document.getElementById('period').value || '';
            const participants = document.getElementById('participants').value || '';

            const keep = getAllItems('keep');
            const problem = getAllItems('problem');
            const tryItems = getAllItems('try');

            let markdown = `# KPT 회고\n\n`;
            markdown += `**회고 일자**: ${date}\n`;
            if (period) markdown += `**회고 기간**: ${period}\n`;
            if (participants) markdown += `**참여자**: ${participants}\n`;
            markdown += `\n---\n\n`;

            markdown += `## Keep (유지할 것)\n\n`;
            if (keep.length > 0) {
                keep.forEach(item => markdown += `- ${item}\n`);
            } else {
                markdown += `- \n`;
            }
            markdown += `\n---\n\n`;

            markdown += `## Problem (문제점)\n\n`;
            if (problem.length > 0) {
                problem.forEach(item => markdown += `- ${item}\n`);
            } else {
                markdown += `- \n`;
            }
            markdown += `\n---\n\n`;

            markdown += `## Try (시도할 것)\n\n`;
            if (tryItems.length > 0) {
                tryItems.forEach(item => markdown += `- ${item}\n`);
            } else {
                markdown += `- \n`;
            }
            markdown += `\n---\n\n`;

            markdown += `## 액션 아이템\n\n`;
            markdown += `| 우선순위 | Try 항목 | 담당자 | 마감일 | 상태 |\n`;
            markdown += `|---------|---------|--------|--------|------|\n`;
            tryItems.forEach((item, index) => {
                markdown += `| ${index + 1} | ${item} | | | |\n`;
            });

            document.getElementById('export-text').value = markdown;
            document.getElementById('export-section').classList.remove('hidden');
            document.getElementById('export-section').scrollIntoView({ behavior: 'smooth' });
        }

        function copyToClipboard() {
            const textarea = document.getElementById('export-text');
            textarea.select();
            document.execCommand('copy');
            alert('클립보드에 복사되었습니다!');
        }

        function saveToLocalStorage() {
            const data = {
                date: document.getElementById('date').value,
                period: document.getElementById('period').value,
                participants: document.getElementById('participants').value,
                keep: getAllItems('keep'),
                problem: getAllItems('problem'),
                try: getAllItems('try')
            };
            localStorage.setItem('kpt-retrospective', JSON.stringify(data));
        }

        function loadFromLocalStorage() {
            const saved = localStorage.getItem('kpt-retrospective');
            if (!saved) {
                alert('저장된 내용이 없습니다.');
                return;
            }

            const data = JSON.parse(saved);
            document.getElementById('date').value = data.date || '';
            document.getElementById('period').value = data.period || '';
            document.getElementById('participants').value = data.participants || '';

            ['keep', 'problem', 'try'].forEach(type => {
                const list = document.getElementById(`${type}-list`);
                list.innerHTML = '';
                itemCounters[type] = 0;
                if (data[type] && data[type].length > 0) {
                    data[type].forEach(item => {
                        addItem(type);
                        const counter = itemCounters[type];
                        document.getElementById(`${type}-input-${counter}`).value = item;
                    });
                }
            });
        }

        function clearAll() {
            if (!confirm('모든 내용을 지우시겠습니까?')) return;

            document.getElementById('date').value = '';
            document.getElementById('period').value = '';
            document.getElementById('participants').value = '';

            ['keep', 'problem', 'try'].forEach(type => {
                document.getElementById(`${type}-list`).innerHTML = '';
                itemCounters[type] = 0;
            });

            localStorage.removeItem('kpt-retrospective');
            document.getElementById('export-section').classList.add('hidden');
        }

        // 자동 저장 (입력 후 1초 지연)
        let saveTimeout;
        document.addEventListener('input', function(e) {
            if (e.target.tagName === 'INPUT' && e.target.type === 'text') {
                clearTimeout(saveTimeout);
                saveTimeout = setTimeout(saveToLocalStorage, 1000);
            }
        });

        // 페이지 로드 시 저장된 내용 불러오기
        window.addEventListener('load', function() {
            const saved = localStorage.getItem('kpt-retrospective');
            if (saved) {
                if (confirm('저장된 내용을 불러오시겠습니까?')) {
                    loadFromLocalStorage();
                }
            }
        });
    </script>
</body>
</html>

```


KPT 회고 도구를 준비했습니다. 다음 파일들이 생성되었습니다:

## 생성된 파일들

1. **README.md** - KPT 회고 방법론 설명과 사용 가이드
2. **template.md** - 마크다운 템플릿 (직접 작성용)
3. **index.html** - 웹 기반 회고 도구 (브라우저에서 사용)

## 사용 방법

### 방법 1: 웹 도구 사용 (추천)
1. `index.html` 파일을 더블클릭하여 브라우저에서 엽니다
2. 상단에 회고 일자, 기간, 참여자를 입력합니다
3. Keep, Problem, Try 섹션에 항목을 추가합니다
4. "마크다운으로 내보내기" 버튼을 클릭하여 결과를 복사합니다
5. 내용은 자동으로 브라우저에 저장됩니다

### 방법 2: 마크다운 템플릿 사용
1. `template.md` 파일을 열어서 직접 작성합니다
2. 각 섹션에 내용을 채워넣습니다

## KPT 회고 진행 순서

1. **Keep 작성**: 이번 기간 동안 잘 되었던 것들을 나열
2. **Problem 작성**: 문제가 되었거나 개선이 필요한 점들을 나열
3. **Try 작성**: Problem에서 도출된 개선 사항들을 구체적인 액션 아이템으로 작성
4. **우선순위 설정**: Try 항목들에 우선순위를 부여하고 담당자와 마감일을 지정
5. **다음 회고에서 검토**: 이전 회고의 Try 항목들이 실제로 시도되었는지 확인

`index.html`을 열어 바로 사용할 수 있습니다. 추가 기능이 필요하면 알려주세요.

