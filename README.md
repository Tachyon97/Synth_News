# NewsSynth - Automated News Article Generator

NewsSynth is a Python application that automates the process of generating and publishing news articles. It fetches articles from one or multiple RSS feeds, generates expanded content and titles using OpenAI's GPT-3 and GPT-4, generates images using DALL-E, and uploads the articles to a WordPress site.

![Starting](output.png)


## Motivation

In the age of information overload, it's important to have tools that can help us process and understand the vast amounts of data available. NewsSynth was created with the goal of automating the process of news article generation and publication, freeing up time and resources for more important tasks. By leveraging the power of AI, NewsSynth can generate high-quality, engaging content in a fraction of the time it would take a human writer.

## Technologies Used

- Python: The main programming language used to develop the application.
- OpenAI's GPT-3 and GPT-4: Used to generate expanded content and titles for each article.
- DALL-E: Used to generate images that represent the content of each article.
- WordPress XML-RPC: Used to upload the generated articles and images to a WordPress site.

## Modules

- `main.py`: The main script that runs the application. It handles the overall control flow, including fetching articles, generating content and titles, generating images, and uploading the articles to a WordPress site.
- `feed.py`: This module is responsible for fetching articles from RSS feeds and generating expanded content and titles using GPT-3 and GPT-4. It interacts with the RSS feed, GPT models, and the `config.json` file to retrieve the necessary information.
- `generate.py`: This module is responsible for generating images that represent the content of each article. It uses DALL-E to generate image descriptions and then generates the corresponding images based on those descriptions.
- `publish.py`: This module handles the uploading of articles and images to a WordPress site using the WordPress XML-RPC library. It connects to the WordPress site, uploads the content and images, and manages the necessary WordPress API calls.
- `config.py`: This module is responsible for loading the configuration from the `config.json` file. It provides functions to access the configuration values, such as the RSS feed URLs, WordPress connection details, and other settings. It ensures that the application uses the correct configuration settings during runtime.
- `utils.py`: This module provides utility functions used throughout the application. It includes functions for handling file paths, loading and saving seen links, and performing other miscellaneous tasks required by the application.

## Setup

1. Clone this repository.
2. Install the required Python packages:
```
pip install -r requirements.txt
```
4. Set up your configuration in the `config.json` file, including RSS feed URLs, WordPress connection details, and other settings.
5. Run `main.py` to start the application.

## Configuration

The configuration for NewsSynth is stored in the `config.json` file. You can modify the following parameters:

- `rss_feed_urls`: A list of RSS feed URLs to fetch articles from.
- `wordpress`: Configuration settings for your WordPress site, including URL, username, password, and categories.
- `loop_delay`: The delay in seconds between each iteration of checking for new articles.
- `folders`: The folders to store prompts and generated images.
- `size`: The size of the generated images.
- `temperature`: The temperature parameter for GPT text generation.
- `max_tokens`: The maximum number of tokens for GPT text generation.

## Contribution

Contributions to NewsSynth are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request. We appreciate your contributions to make NewsSynth even better.

## Future Updates


- **Multiple RSS Feeds**: We plan to enhance the application to support multiple RSS feeds. This will enable users to fetch articles from different sources and expand the scope of generated content.
- **Improved Image Generation**: We're looking into ways to improve the image generation process, such as allowing users to specify the type of image they want (e.g., illustration, photo), the color scheme, etc.

## Development Log

- **Version 1.01**: Modularization and configuration file support. The application has been modularized into separate scripts to handle different functionalities. It now uses a configuration file (`config.json`) to manage various settings such as WordPress connection details, RSS feed URLs, etc.
- **Version 1.0**: Initial release. The application can fetch articles from RSS feeds, generate expanded content and titles using GPT-3 and GPT-4, generate images using DALL-E, and upload the articles to a WordPress site.

## License

This project is licensed under the terms of the MIT license.