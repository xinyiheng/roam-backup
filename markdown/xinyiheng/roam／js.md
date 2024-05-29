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
(async () => {
    // Function to fetch all notes from Roam
    async function fetchAllNotes() {
        const allPagesQuery = `[:find (pull ?page [:node/title {:block/children [:block/string]}])
                                :where [?page :node/title]]`;
        const result = await window.roamAlphaAPI.q(allPagesQuery);
        return result.map(page => page[0]).filter(note => {
            const noteContent = note.children ? note.children.map(child => child.string).join(' ') : '';
            return noteContent.length > 30;
        });
    }

    // Function to select a random note
    function getRandomNote(notes) {
        const randomIndex = Math.floor(Math.random() * notes.length);
        return notes[randomIndex];
    }

    // Function to create a note card element
    function createNoteCard(note) {
        const card = document.createElement('div');
        card.style.border = '1px solid #ccc';
        card.style.borderRadius = '8px';
        card.style.padding = '16px';
        card.style.margin = '16px';
        card.style.boxShadow = '0 2px 4px rgba(0, 0, 0, 0.1)';
        card.style.backgroundColor = 'white';

        const title = document.createElement('h3');
        title.innerText = note.title || 'Untitled';
        card.appendChild(title);

        if (note.children) {
            const content = document.createElement('p');
            content.innerText = note.children.map(child => child.string).join('\n');
            card.appendChild(content);
        }

        return card;
    }

    // Function to display a random note
    async function displayRandomNote() {
        const allNotes = await fetchAllNotes();
        const randomNote = getRandomNote(allNotes);
        if (randomNote) {
            const noteCard = createNoteCard(randomNote);
            const container = document.getElementById('random-note-container');
            container.innerHTML = '';  // Clear previous note
            container.appendChild(noteCard);
        } else {
            alert('No notes found with more than 30 characters.');
        }
    }

    // Create a button in Roam's sidebar to trigger random note browsing
    function createRandomNoteButton() {
        const sidebar = document.querySelector('.roam-sidebar-container .roam-article');
        if (!sidebar) return;

        const button = document.createElement('button');
        button.innerText = 'Browse Random Note';
        button.style.display = 'block';
        button.style.margin = '10px 0';
        button.style.padding = '10px';
        button.style.backgroundColor = '#007bff';
        button.style.color = 'white';
        button.style.border = 'none';
        button.style.borderRadius = '4px';
        button.onclick = displayRandomNote;
        
        sidebar.insertBefore(button, sidebar.firstChild);
    }

    // Create a container for the random note
    function createRandomNoteContainer() {
        const container = document.createElement('div');
        container.id = 'random-note-container';
        container.style.position = 'fixed';
        container.style.bottom = '10px';
        container.style.right = '10px';
        container.style.width = '300px';
        container.style.maxHeight = '400px';
        container.style.overflowY = 'auto';
        container.style.zIndex = 1000;
        container.style.backgroundColor = 'white';
        container.style.padding = '10px';
        container.style.border = '1px solid #ccc';
        container.style.borderRadius = '8px';
        container.style.boxShadow = '0 2px 4px rgba(0, 0, 0, 0.1)';
        document.body.appendChild(container);
    }

    // Initialize the plugin
    function init() {
        createRandomNoteButton();
        createRandomNoteContainer();
    }

    // Run the plugin
    init();
})();
```
