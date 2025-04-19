# My Documents

A personal repository to store and organize markdown documents, hosted using GitHub Pages with the Minima theme.

## Structure

The repository is organized into the following main categories:

*   `daily_planning/`: Notes and plans for daily activities.
*   `research/`: Findings and notes from research topics.
*   `shopping/`: Shopping lists and related notes.
*   `trips/`: Plans and logs for trips.

## Usage

*   **Content:** Documents are written in Markdown (`.md`).
*   **GitHub Pages:** The site is automatically built and deployed by GitHub Pages when changes are pushed to the main branch.
*   **Theme:** Uses the default Jekyll `minima` theme. See `_config.yml`.
*   **Homepage:** The main entry point is `index.md`, which uses the theme's `home` layout.

## Demo

Check out the live demo of the site at: [https://alianjum0.github.io/my-documents](https://alianjum0.github.io/my-documents)

## Local Development with Docker Compose

To run the site locally using Docker Compose:

1. **Ensure Docker and Docker Compose are installed and running correctly.**
2. Run the following command from the project root directory:

    ```bash
    docker-compose up
    ```

3. Open `http://localhost:4000` in your browser.

This will start the Jekyll server using Docker Compose, allowing you to preview the site locally.

*   **`Gemfile`:** Specifies the Jekyll version and necessary gems (like `webrick` for local serving). `bundle install` (run inside the Docker command) installs these gems.
*   **`vendor/bundle`:** This directory (created when running the Docker command) caches installed gems to speed up subsequent builds. It's included in `.gitignore`.

## Formatting & Linting

This project uses [Markdownlint](https://github.com/DavidAnson/markdownlint) to ensure consistent Markdown formatting.

*   **Configuration:** Rules are defined in `.markdownlint.json`.
*   **Usage:** You can run a linter locally (e.g., using VS Code extensions or the `markdownlint-cli` tool) to check files before committing. (Consider adding a GitHub Action later for automated checks).

## Contributing

This is primarily a personal repository, but suggestions or corrections are welcome via issues or pull requests.

## License

This project's content (unless otherwise specified within individual documents) is licensed under the [MIT License](LICENSE).
