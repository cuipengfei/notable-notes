---
tags: [code-snippet, geek-time]
title: export geek time notes
created: '2023-12-10T12:37:22.555Z'
modified: '2023-12-10T13:14:45.080Z'
---

# export geek time notes

```js
var chapters=document.getElementsByClassName("step_step-content_Eajwz")
var notesContent=""; 
for (var i = chapters.length-1; i >=0; i--) {
    var chapter = chapters[i];
    var chapterTitle=chapter.getElementsByClassName("LessonNoteItemPc_lesson-title_3GvJ3")[0].innerText;
    notesContent+="## "+chapterTitle+"\n\n";
 
    var notes = chapter.getElementsByClassName("BarNotePc_note-source_13AV1");
    for (var j=notes.length-1; j>=0; j--){
      notesContent+=notes[j].innerText+"\n\n";
    }
}

console.log(notesContent);
```


