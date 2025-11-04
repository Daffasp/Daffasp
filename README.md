# Hi 👋, I'm <span style="color:#FF6F61;">Daffa Sadewa Putra</span> ✨

## About Me
I'm a passionate **Software Developer & Tech Enthusiast**.  
I love creating **web apps**, exploring **new technologies**, and learning **every day**.  

## 🌟 Fun Facts
- 💻 Currently exploring **VueJS, CodeIgniter 4 & MongoDB**
- 🎨 Enjoy designing clean **UI/UX**
- 🌱 Always learning **new programming skills**
- 📫 You can reach me via GitHub issues or email

---

<!-- Animated typing effect using GitHub-supported HTML -->
<p>
  <b>Current Mood:</b>
  <span id="animatedText"></span>
</p>

<script>
const text = ["Coding 💻", "Learning 📚", "Creating 🎨", "Exploring 🌍"];
let i = 0, j = 0, currentText = "", isDeleting = false;
const speed = 100;

function type() {
    if (i < text.length) {
        if (!isDeleting && j <= text[i].length) {
            currentText = text[i].substring(0, j++);
            document.getElementById("animatedText").innerText = currentText;
        } else if (isDeleting && j >= 0) {
            currentText = text[i].substring(0, j--);
            document.getElementById("animatedText").innerText = currentText;
        }

        if (j === text[i].length) { isDeleting = true; setTimeout(type, 500); return; }
        if (isDeleting && j === 0) { isDeleting = false; i = (i + 1) % text.length; }
    }
    setTimeout(type, speed);
}
type();
</script>
