#  Debrid Media

All you need to run a Plex media server with Real-Debrid.

##  Prerequisites


- Real-Debrid premium account

- Plex account

  

##  Setup

  

1.  **Configure environment variables**

- Rename `.env.example` to `.env`

- Set `TZ` to your timezone

- Adjust `RCLONE_CACHE_LIMIT` to match the disk space you can dedicate to caching (e.g. `10G`)

- Visit <https://plex.tv/claim> while signed in and copy the claim token into `PLEX_CLAIM`

2.  **Provide your Real-Debrid API key**

- Open `config/config.yml`

- Replace `token` with key from <https://real-debrid.com/devices>

3.  **Launch the stack**

- Run `docker compose up -d`

4.  **Plex setup**

- Open `http://<your_server_ip>:32400/web` to complete the setup

- Choose `Add Library`, pick `Movies`, `TV Shows`, or `Other Videos`, and find them under `/data`

- Go to Plex `Settings` → `Library` and change `Library scan interval` to every 15 minutes
  

##  What's Next

Visit <https://debridmediamanager.com>, add the movies or shows you want, and wait them to appear in your Plex media server