<!DOCTYPE html>
<html>
<head>
    <title>Devotional Stories E-Book</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f4f4f4;
            margin: 0;
            padding: 0;
        }

        header {
            background: #8b4513;
            color: white;
            text-align: center;
            padding: 20px;
        }

        .container {
            width: 90%;
            max-width: 900px;
            margin: auto;
            padding: 20px;
        }

        .story {
            background: white;
            padding: 20px;
            margin-bottom: 20px;
            border-radius: 10px;
            box-shadow: 0 0 5px gray;
        }

        .story h2 {
            color: #8b4513;
        }

        footer {
            background: #8b4513;
            color: white;
            text-align: center;
            padding: 15px;
        }

        button {
            background: #8b4513;
            color: white;
            border: none;
            padding: 10px 15px;
            cursor: pointer;
            border-radius: 5px;
        }

        button:hover {
            background: #a0522d;
        }

        #addStory {
            background: white;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
        }

        textarea, input {
            width: 100%;
            margin-top: 10px;
            margin-bottom: 10px;
            padding: 10px;
        }
    </style>
</head>

<body>

<header>
    <h1>📖 Devotional Stories E-Book</h1>
    <p>Read inspiring devotional stories</p>
</header>

<div class="container">

    <div id="addStory">
        <h2>Add New Story</h2>

        <input type="text" id="title" placeholder="Story Title">

        <textarea id="content" rows="6"
            placeholder="Write your devotional story here..."></textarea>

        <button onclick="addStory()">Publish Story</button>
    </div>

    <div id="stories">

        <div class="story">
            <h2>Faith and Courage</h2>
            <p>
                A young devotee trusted God during difficult times and
                found strength through prayer and faith.
            </p>
        </div>

    </div>

</div>

<footer>
    © 2026 Devotional Stories E-Book
</footer>

<script>
function addStory() {

    let title = document.getElementById("title").value;
    let content = document.getElementById("content").value;

    if(title === "" || content === "") {
        alert("Please enter title and story.");
        return;
    }

    let storyDiv = document.createElement("div");
    storyDiv.className = "story";

    storyDiv.innerHTML =
        "<h2>" + title + "</h2>" +
        "<p>" + content + "</p>";

    document.getElementById("stories")
        .prepend(storyDiv);

    document.getElementById("title").value = "";
    document.getElementById("content").value = "";
}
</script>

</body>
</html>
