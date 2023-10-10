- 下一个文本
    - {{[[roam/js]]}}
        - ```javascript
function openNextBlock() {
    const selectedBlock = document.querySelector(".roam-block-focused");
    if (!selectedBlock) {
        console.log("No block is currently selected.");
        return;
    }
    const nextBlock = selectedBlock.parentElement.nextSibling;
    if (!nextBlock) {
        console.log("There is no next block.");
        return;
    }
    nextBlock.querySelector(".roam-block").click();
}

function createSidebarButton() {
    if (!document.getElementById('openNextBlockButton')) {
        const button = document.createElement('div');
        button.classList.add('log-button');
        button.innerHTML = "Open Next Block";
        button.id = 'openNextBlockButton';
        const icon = document.createElement('span');
        icon.classList.add('bp3-icon', 'bp3-icon-step-forward', 'icon');
        button.prepend(icon);
        const sidebarContent = document.querySelector("#app > div.roam-body > div.roam-app > div.roam-sidebar-container.noselect > div");
        const sidebarTopRow = sidebarContent.childNodes[1];
        if (sidebarContent && sidebarTopRow) {
            sidebarTopRow.parentNode.insertBefore(button, sidebarTopRow.nextSibling);
        }
        button.onclick = openNextBlock;
    }
}

createSidebarButton();
```
