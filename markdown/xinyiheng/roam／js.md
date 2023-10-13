- 随机卡片快捷键
    - {{[[roam/js]]}}
        - ```javascript
document.addEventListener('keydown', function(e) {
    // 检查是否按下了 'Command', 'Shift' 和 'ArrowRight' 键
    if (e.metaKey && e.shiftKey && e.key === 'ArrowRight') {
        // 根据 id 'randomDiv' 查找 "Random Block" 按钮并点击它
        const randomBlockButton = document.getElementById('randomDiv');
        if (randomBlockButton) {
            randomBlockButton.click();
        }
    }
});

```
- 随机
    - {{[[roam/js]]}}
        - ```javascript
function togglerandom() {
    // 弹出对话框询问用户要查询的data-page-title
    var pageTitle = prompt("请输入要查询的data-page-title：");
    console.log("输入的data-page-title:", pageTitle);

    // 使用Roam API查询特定data-page-title下的block
    var blocks = window.roamAlphaAPI.q(`[:find [(rand 1 ?block-uid)] :where [?e :block/page ?page-title] [?e :block/uid ?block-uid] [(= "${pageTitle}" ?page-title)]]`);
    console.log("查询结果:", blocks);

    // 如果找到了block
    if (blocks.length > 0) {
        var randomBlockUid = blocks[0][0];
        console.log("随机选择的block UID:", randomBlockUid);
        window.roamAlphaAPI.ui.mainWindow.openBlock({ block: { uid: randomBlockUid } });
    } else {
        alert("未找到与该data-page-title匹配的block。");
    }
}
```
