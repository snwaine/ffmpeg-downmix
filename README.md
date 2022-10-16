services:
  ffmpeg-watch:
    container_name: ffmpeg-watch
    image: labithiotis/ffmpeg-watch
    restart: always
    environment:
      ENCODER: libx265
      CRF: 28
      PRESET: verfast
      EXTENSION: mp4
    volumes:
      - 'PATH_TO_STORAGE:/storage'
      - 'PATH_TO_WATCH:/watch'
      - 'PATH_TO_OUTPUT:/output'
