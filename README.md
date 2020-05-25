# Audio-Mood-Prediction
Predicts the mood of an audio file as party,happy,sad or romantic.

Requirements:

 <li> Python 3.7</li>
 <li>numpy
 <li> pandas
 <li> sklearn
 <li>matplotlib
 <li>pyAudioAnalysis (pip install pydub)
 <li>eyed3 (pip install eyed3)
 <li>ffmpeg (conda install -c conda-forge ffmpeg)
 <li>pickle
 <li>seaborn
 
Execution: Run "predictAudioMood.py"

Algorithm:

<li>Extract useful features from the music by pre-processing the mp3 file.
<li>Use Semi-supervised learning with k-Means clustering to segregate and label the audio files into one of the moods.
<li>An ensemble of XGBoost and SVM models predict the mood of an audio file. All the machine learning algorithms were implemented from scratch.
<li>The trained models are stored using pickle.
<li>"predictAudioMood.py" accepts an input song and outputs predicted mood for the song.


File descriptions:

<li>getDataSet.py Feature Extraction from mp3 files. Output is stored in MusicData.csv
<li>getNoOfClusters.py Prints the elbow method graph for number of clusters = 1 to 10
<li>kMeans.py Peforms clustering of data. Output is stored in LabelledMusicData.csv
<li>XGBoost.py Creates the XGBoost model
<li>SVM.py Creates the SVM model
<li>getMetrics Utility function to get the different metrics of the algorithms
<li>PrintMetrics.py Prints all the different metrics of the algorithms
<li>predictAudioMood.py Predicts the mood of an audio file
