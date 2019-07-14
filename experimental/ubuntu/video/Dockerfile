FROM databricksruntime/dbfsfuse-py3:latest

# update add ppa repo with ffmpeg version 3
RUN apt-get update && apt-get install -y software-properties-common

RUN add-apt-repository -y ppa:jonathonf/ffmpeg-3  && apt update \
  && apt-get install -y \
	ffmpeg \
	libavformat-dev \
	libavcodec-dev \
	libavdevice-dev \
	libavutil-dev \
	libswscale-dev \
	libswresample-dev \
	libavfilter-dev \
	libav-tools \
	pkg-config \
        python-dev \
	python3-dev \
	x264 \
	x265 \
  && rm -rf /var/lib/apt/lists/*

RUN /databricks/python3/bin/pip install \
	av \
	ffmpeg-python \
	imageio \
	opencv-python \
	pims
