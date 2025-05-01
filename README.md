# Pinchflat YouTube Audio Downloader

A self-hosted solution for downloading audio from YouTube channels and playlists using Pinchflat.

## What is Pinchflat?

Pinchflat is a self-hosted app for downloading YouTube content built using yt-dlp. This repository contains configuration files to deploy Pinchflat specifically for audio downloads.

## Features

- Downloads audio from YouTube channels and playlists
- Extracts high-quality MP3 audio from videos
- Embeds thumbnails and metadata in the audio files
- Periodically checks for new content
- Simple web-based UI for management

## Deployment

This repository is configured for deployment with Coolify. For full instructions, see the [Coolify documentation](https://coolify.io/docs).

### Quick Start

1. In Coolify, create a new resource pointing to this repository
2. Select "Docker Compose" as the build pack
3. Set base directory to `/` and Docker Compose location to `/docker-compose.yml`
4. Deploy the stack
5. Access Pinchflat at the URL provided by Coolify

## Configuration

After deployment, configure Pinchflat with the following settings:

1. Create a Media Profile for audio downloads
   - Name it "Audio Only"
   - Set the Output path template to include MP3 extension: `${channel_name}/${title}.mp3`

2. Add YouTube channels or playlists as Sources
   - Each Source should use the "Audio Only" media profile

## License

This repository contains configuration files only. Pinchflat is created by [Kieran Eglin](https://github.com/kieraneglin/pinchflat).
