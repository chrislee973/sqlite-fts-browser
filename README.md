# SQLite FTS In The Browser

This is a proof of concept running full-text search on a SQLite database in the browser using a custom FTS5-enabled build of [sql.js](https://github.com/chrislee973/sql.js). The transcript display and search functionality is all done via sql queries running in your browser.

The data source we use here is a sqlite database I pregenerated of the transcript for this youtube video: https://www.youtube.com/watch?v=-nckO_vl2_U. This file is served from `public/creatorsupport.db`

## Local Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/chrislee973/sqlite-fts-browser.git
   cd sqlite-fts-browser/public
   ```

2. Serve the files using a local web server. For example, using Python:

   ```bash
   # Python 3
   python -m http.server 8080
   ```

3. Open your browser and navigate to:
   ```
   http://localhost:8000
   ```

Note: You must serve the files through a web server rather than opening the HTML file directly in your filesytem, due to browser security restrictions when loading the SQL.js WASM module. Also, the code is in the `public` folder because we're deploying to Vercel as a static site and Vercel expects static assets to be in the public folder.
