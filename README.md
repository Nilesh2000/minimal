# Minimal Hugo Theme

Minimal is a clean, responsive, and minimalistic theme for Hugo. The aim was to have a theme that is simple to customize and centered around the content.

![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)
![Hugo Version](https://img.shields.io/badge/Hugo-0.116.0+-blue.svg?style=flat-square)

## Features

- Dark/Light mode toggle
- Fully responsive
- Fast and lightweight
- Reading time calculation
- Social Links Integration
- Analytics Configuration with Umami

## Setup

1. **Create a new Hugo site:**
   ```bash
   hugo new site <your-site-name> --config
   ```

2. **Add the theme to your site:**
   ```bash
   cd <your-site-name>
   git submodule add --depth=1 https://github.com/Nilesh2000/minimal.git themes/minimal
   git submodule update --init --recursive
   ```

3. **Configure `hugo.toml`:**
Here is a sample config:
```toml
[params]
# Homepage content
homepageContent = """
# Welcome to My Site

This is the homepage content that can be configured in the site config.

You can add any markdown content here, including **bold text**, *italic text*, and [links](https://example.com).
"""

# Umami Analytics configuration
[params.umami]
enabled = true
jsLocation = "<your-umami-script-url>"
websiteId = "<your-umami-website-id>"

# Navigation menu configuration
[[params.menu]]
name = 'Home'
url = '/'
weight = 10

[[params.menu]]
name = 'Posts'
url = '/posts'
weight = 20

# Social links - flexible configuration
[[params.social]]
name = "GitHub"
url = "https://github.com/yourusername"
icon = "fa-brands fa-github"
aria_label = "GitHub"

[[params.social]]
name = "Email"
url = "mailto:your.email@example.com"
icon = "fa-solid fa-envelope"
aria_label = "Email"
```

4. **Start the server:**
```bash
hugo server -D
```

5. **Add content to your site:**
```bash
hugo new posts/my-first-post.md
```

## Support

If you have any questions or need help, please open an issue on [GitHub](https://github.com/Nilesh2000/minimal/issues).
If you use the theme or found it useful you can support me by leaving a star

## License

MIT License - see [LICENSE](LICENSE) file for details.
