# Speech-Emotion-Recognition


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>Audio Emotion Recognition</h1>
    <p>This project focuses on recognizing emotions from audio signals using various data processing, feature extraction, and machine learning techniques. The dataset was sourced from Kaggle and the analysis was performed in Google Colab.</p>

  <h2>Dataset</h2>
    <p>The dataset used for this project was obtained from <a href="https://www.kaggle.com/">Kaggle</a>. It contains audio files labeled with different emotions.</p>

  <h2>Data Processing and Augmentation</h2>
    <p>To prepare the dataset for analysis, I performed the following steps:</p>
    <ol>
        <li>Imported the dataset into Google Colab.</li>
        <li>Extracted the different 'emotions' from the dataset.</li>
        <li>Generated spectrograms for each audio file to analyze how they change over time.</li>
        <li>Applied data augmentation techniques to enhance the dataset:
            <ul>
                <li><strong>TimeStretch</strong>: To simulate variations in speech speed.</li>
                <li><strong>PitchShift</strong>: To simulate changes in pitch.</li>
                <li><strong>AddNoise</strong>: To simulate background noise.</li>
                <li><strong>TimeShift</strong>: To shift the audio in time.</li>
            </ul>
        </li>
    </ol>
    <p>These augmentation techniques helped increase the data size, simulate real-world variations, balance class distribution, and enhance model accuracy.</p>

  <h2>Feature Extraction</h2>
    <p>The audio signal, a three-dimensional signal with time, amplitude, and frequency axes, required feature extraction. The following features were extracted:</p>
    <ul>
        <li>Zero-Crossing Rate</li>
        <li>Energy Entropy</li>
        <li>Spectral Flux</li>
        <li>Spectral Roll-off</li>
        <li>Spectral Centroid</li>
        <li>Chroma</li>
        <li>Mel-Frequency Cepstral Coefficients (MFCC)</li>
    </ul>
    <p>The numerical values of these features were added to a data frame for further analysis.</p>

   <h2>Feature Engineering</h2>
    <p>To improve model performance, feature engineering was performed:</p>
    <ul>
        <li>Removed unwanted features due to high correlation (e.g., either zero-crossing rate or spectral centroid).</li>
    </ul>

  <h2>Data Normalization and Splitting</h2>
    <p>The data was then normalized and split into training and testing sets. A scaler was used to apply a fit transform on the data.</p>

  <h2>Model Training</h2>
    <p>The processed dataset was fed into a machine learning model. The model was compiled and trained.. Increasing the number of epochs beyond 100 can yield even better results.</p>

  <h2>Conclusion</h2>
    <p>This project demonstrated the effective use of data processing, augmentation, feature extraction, and machine learning techniques in recognizing emotions from audio signals. Further improvements can be made by fine-tuning the model and exploring additional features.</p>


  <h2>References</h2>
    <ul>
        <li><a href="https://devopedia.org/audio-feature-extraction">https://devopedia.org/audio-feature-extraction</a></li>
        <li><a href="https://www.kaggle.com/">Kaggle Dataset</a></li>
        <li><a href="https://colab.research.google.com/">Google Colab</a></li>
        <li><a href="https://towardsdatascience.com/extract-features-of-music-75a3f9bc265d/">https://towardsdatascience.com/extract-features-of-music-75a3f9bc265d</a></li>
        <li><a href="https://medium.com/@makcedward/data-augmentation-for-audio-76912b01fdf6">https://medium.com/@makcedward/data-augmentation-for-audio-76912b01fdf6</a></li>
    </ul>

  <h2>License</h2>
    <p>This project is licensed under the MIT License - see the <a href="LICENSE">LICENSE</a> file for details.</p>
</body>
</html>
