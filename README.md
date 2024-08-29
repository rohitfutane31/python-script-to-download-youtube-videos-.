# project-7-python-script-to-download-youtube-videos-.

python script to download youtube videos 

Code Description:
This Python script performs several tasks related to YouTube videos, such as extracting information about the video and providing an option to download it. The script uses two libraries: pytube and yt-dlp.
Step-by-Step Breakdown
1.	Installing Required Packages:
o	pip install pytube3 and pip install --upgrade pytube: Install and upgrade the pytube library. This library allows you to interact with YouTube videos.
o	pip install yt-dlp: Install yt-dlp, a popular YouTube downloader with more advanced features.
2.	Importing the Libraries:
o	from pytube import YouTube: Import the YouTube class from the pytube library, which is used to interact with YouTube videos.
o	from yt_dlp import YoutubeDL: Import the YoutubeDL class from yt-dlp, used for downloading videos.
3.	Getting the YouTube Video Link:
o	link = input("Enter youtube video"): Prompt the user to enter the YouTube video URL.
4.	Extracting Video Information:
o	yt = YouTube(link): Create a YouTube object for the provided video link.
o	print("Title :", yt.title): Print the title of the video.
o	print("Views :", yt.views): Print the number of views the video has.
o	print("Duration :", yt.length): Print the duration (in seconds) of the video.
o	print("Description :", yt.description): Print the video's description.
o	print("Ratings :", yt.rating): Print the video's average rating.
5.	Downloading the Video:
o	download_option = input("Do you want to download this video? (yes/no): ").lower(): Ask the user if they want to download the video. The answer is converted to lowercase for easier comparison.
o	If the user chooses "yes":
	url = 'https://youtube.com/shorts/skdXa3Q61HE?si=nHklaHieslhrsGxm': Define the URL of the video to be downloaded (in this case, a specific YouTube Shorts video).
	ydl_opts = {'format': 'best'}: Set the download options, specifying that the best quality available should be downloaded.
	with YoutubeDL(ydl_opts) as ydl: Use the YoutubeDL class to download the video using the specified options.
	ydl.download([url]): Start downloading the video.
	print("Download completed."): Inform the user that the download is complete.
o	If the user chooses "no":
	print("Download aborted."): Inform the user that the download has been aborted.

