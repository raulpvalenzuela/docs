# youtube-dl

- Basic Download:

  ```bash
  youtube-dl [URL]
  ```

- Download from list in file:

  ```bash
  youtube-dl -a youtube_links.txt
  ```

- Download Playlist, put in folder, and index with order:

  ```bash
  youtube-dl -o '%(playlist)s/%(playlist_index)s - %(title)s.%(ext)s' [URL]
  ```

- Download to `/uploader/date/title.ext`:

  ```bash
  youtube-dl -o '%(uploader)s/%(date)s/%(title)s.%(ext)s' [URL]
  ```

- Download playlist starting from certain video:

  ```bash
  youtube-dl --playlist-start 5 [URL]

- Simulate download:

  ```bash
  youtube-dl -s [URL]
  ```

- Download audio only in mp3 format

  ```bash
  youtube-dl -x --audio-format "mp3" [URL]
  ```
