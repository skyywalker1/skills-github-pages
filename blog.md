<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog | Heartland Haven Farm</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            color: #333;
        }

        header {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 30px 20px;
        }

        header h1 {
            margin: 0;
            font-size: 2.5em;
        }

        .blog-container {
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            background-color: white;
            border-radius: 8px;
        }

        .blog-post-title {
            font-size: 1.8em;
            color: #333;
            margin-bottom: 10px;
        }

        .blog-post-excerpt {
            font-size: 1.2em;
            color: #555;
            margin-bottom: 20px;
        }

        .blog-post-link {
            color: #1a73e8;
            text-decoration: none;
        }

        .blog-post-link:hover {
            text-decoration: underline;
        }

        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: white;
            margin-top: 40px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Heartland Haven Farm Blog</h1>
        <p>Your Guide to Sustainable Living</p>
    </header>

    <div class="blog-container">
        <h2>Latest Blog Posts</h2>

        <!-- Jekyll loop to display posts -->
        {% for post in site.posts %}
            <div class="blog-post">
                <h3 class="blog-post-title">
                    <a href="{{ post.url }}" class="blog-post-link">{{ post.title }}</a>
                </h3>
                <p class="blog-post-excerpt">{{ post.excerpt }}</p>
                <p><a href="{{ post.url }}" class="blog-post-link">Read more...</a></p>
            </div>
        {% endfor %}
    </div>

    <footer>
        <p>&copy; 2025 Heartland Haven Farm. All rights reserved.</p>
    </footer>

</body>
</html>
