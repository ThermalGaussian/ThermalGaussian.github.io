## THERMALGAUSSIAN :THERMAL 3D GAUSSIAN SPLATTING

![alt text](NaturalDubber.png)


## Abstract
Thermography is especially valuable for the military and other users of surveillance cameras. Some recent methods based on Neural Radiance Fields (NeRF) are
proposed to reconstruct the thermal scenes in 3D from a set of thermal and RGB images. However, unlike NeRF, 3D Gaussian splatting (3DGS) prevails due to its
rapid training and real-time rendering. In this work, we propose ThermalGaussian, the first thermal 3DGS approach capable of rendering high-quality images in
RGB and thermal modalities. We first calibrate the RGB camera and the thermal camera to ensure that both modalities are accurately aligned. Subsequently, we use the registered images to learn the multimodal 3D Gaussians. To prevent the overfitting of any single modality, we introduce several multimodal regularization
constraints. We also develop smoothing constraints tailored to the physical characteristics of the thermal modality. Besides, we contribute a real-world dataset
named RGBT-Scenes, captured by a hand-hold thermal-infrared camera, facilitating future research on thermal scene reconstruction. We conduct comprehensive experiments to show that ThermalGaussian achieves photorealistic rendering of thermal images and improves the rendering quality of RGB images. With the proposed multimodal regularization constraints, we also reduced the model’s storage cost by 90%. The code and dataset will be released.


<a id="Setting1V2C"></a>

### V2C-Animation sample on Dub 1.0
### Sample #1
#### Script: Every night it sneaks in my yard and gobbles my poor azaleas.
<table border="1">
    <tr>
        <td>
<video width="330" height="170" controls>
  <source src="Setting1\Sample1\StyleSpeech_Up@Carl_00_0152_00.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>StyleSpeech</figcaption>
        </td>
        <td>
<video  width="330" height="170" controls>
  <source src="Setting1\Sample1\ZeroshotTTS_Up@Carl_00_0152_00.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Zeroshot-TTS</figcaption>
        </td>
        <td>
<video  width="330" height="170" controls>
  <source src="Setting1\Sample1\V2C-Net_Up@Carl_00_0152_00.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>V2C-Net</figcaption>
        </td>
    </tr>
    <tr>
        <td>
<video  width="330" height="170" controls>
  <source src="Setting1\Sample1\HPMDubbing_Up@Carl_00_0152_00.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>HPMDubbing</figcaption>
        </td>
        <td>
<video  width="330" height="170" controls>
  <source src="Setting1\Sample1\Ours_Up@Carl_00_0152_00.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Ours</figcaption>
        </td>
        <td>
<video  width="330" height="170" controls>
  <source src="Setting1\Sample1\Up@Carl_00_0152_00.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>GT</figcaption>
        </td>
    </tr>
</table>

### Sample #2
#### Script: This is very serious.
<table border="1">
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample2\StyleSpeech.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>StyleSpeech</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample2\Zeroshot_TTS.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Zeroshot-TTS</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample2\V2C-Net.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>V2C-Net</figcaption>
        </td>
    </tr>
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample2\HPMdubbing.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>HPMDubbing</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample2\Ours.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Ours</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample2\Setting1Sample2.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>GT</figcaption>
        </td>
    </tr>
</table>


### Sample #3
#### Script: Everyone wants the hot, new thing.
<table border="1">
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample3\StyleSpeech.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>StyleSpeech</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample3\Zeroshot_TTS.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Zeroshot-TTS</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample3\V2C-Net.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>V2C-Net</figcaption>
        </td>
    </tr>
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample3\HPMDubbing.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>HPMDubbing</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample3\ours.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Ours</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting1\sample3\Bossbaby@BossBaby_00_0241_00.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>GT</figcaption>
        </td>
    </tr>
</table>

<a id="Setting1GRID"></a>

### GRID sample on Dub 1.0
#### Script: bin blue at s three again
<table border="1">
    <tr>
        <td>
<video width="320" height="200" controls>
  <source src="Setting1\sample4\Style.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>StyleSpeech</figcaption>
        </td>
        <td>
<video width="320" height="200" controls>
  <source src="Setting1\sample4\ZeroshotTTS.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Zeroshot-TTS</figcaption>
        </td>
        <td>
<video width="320" height="200" controls>
  <source src="Setting1\sample4\V2C-Net.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>V2C-Net</figcaption>
        </td>
    </tr>
    <tr>
        <td>
<video width="320" height="200" controls>
  <source src="Setting1\sample4\HPMDubbing.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>HPMDubbing</figcaption>
        </td>
        <td>
<video width="320" height="200" controls>
  <source src="Setting1\sample4\Ours.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Ours</figcaption>
        </td>
        <td>
<video width="320" height="200" controls>
  <source src="Setting1\sample4\GT.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>GT</figcaption>
        </td>
    </tr>
</table>


<a id="Setting2V2C"></a>

### V2C-Animation sample on Dub 2.0
### Sample #1
#### Script: Sentient food? That's impossible.
Reference Audio：

<audio controls src="Setting2/sample1/Cloudy@Flint_00_0134_00.wav" title="Title"></audio>
<table border="1">
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample1\style.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>StyleSpeech</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample1\zeroshottts.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Zeroshot-TTS</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample1\V2C-Net.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>V2C-Net</figcaption>
        </td>
    </tr>
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample1\HPMDubbing.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>HPMDubbing</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample1\Ours.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Ours</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample1\GT.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>GT</figcaption>
        </td>
    </tr>
</table>



### Sample #2
#### Script: Here's what I heard: "Blah, blah, blah."
Reference Audio：

<audio controls src="Setting2\sample2\Cloudy@Mayor_00_0844_00.wav" title="Title"></audio>

<table border="1">
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample2\Style.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>StyleSpeech</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample2\Zeroshot.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Zeroshot-TTS</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample2\V2Cnet.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>V2C-Net</figcaption>
        </td>
    </tr>
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample2\HPMDubbing.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>HPMDubbing</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample2\Ours.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Ours</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample2\GT.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>GT</figcaption>
        </td>
    </tr>
</table>

### Sample #3
#### Script: Well, I just saved our lives.
<audio controls src="Setting2/sample3/Inside@Disgust_00_0772_00.wav" title="Title"></audio>
<table border="1">
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample3\style.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>StyleSpeech</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample3\zeroshot.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Zeroshot-TTS</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample3\VC.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>V2C-Net</figcaption>
        </td>
    </tr>
    <tr>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample3\HPMDubbing.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>HPMDubbing</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample3\ours.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>Ours</figcaption>
        </td>
        <td>
<video width="320" height="140" controls>
  <source src="Setting2\sample3\GT.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<figcaption>GT</figcaption>
        </td>
    </tr>
</table>

<a id="zeroshot"></a>

### Zero-shot sample test
### Sample #1
#### Script: How do we know that this isn't some trick?
#### Ground truth:
<video width="320" height="140" controls>
  <source src="zeroshot\sample1\gt.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<!-- <video controls src="zeroshot\sample1\gt.mp4" title="Title"></video> -->
<table border="1">
  <tr>
    <td>
      <audio controls>
        <source src="zeroshot\sample1\s4-pwwq7p.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #1</figcaption>
    </td>
    <td>
      <audio controls>
        <source src="zeroshot\sample1\s9-bbwz4n.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #2</figcaption>
    </td>
    <td>
      <audio controls>
        <source src="zeroshot\sample1\s15-pwbv7a.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #3</figcaption>
    </td>
  </tr>
  <tr>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample1\zeroshot_s4.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample1\zeroshot_s9.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample1\zeroshot_s15.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
  </tr>
</table>

### Sample #2
#### Script: Now what?
#### Ground truth:
<video width="320" height="140" controls>
  <source src="zeroshot\sample2\gt.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<table border="1">
  <tr>
    <td>
      <audio controls>
        <source src="zeroshot\sample2\s14-swbn7p.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #1</figcaption>
    </td>
    <td>
      <audio controls>
        <source src="zeroshot\sample2\s22-lrbxza.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #2</figcaption>
    </td>
    <td>
      <audio controls>
        <source src="zeroshot\sample2\s30-sgwg7p.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #3</figcaption>
    </td>
  </tr>
  <tr>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample2\s14.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample2\s22.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample2\s30.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
  </tr>
</table>

### Sample #3
#### Script: It's a lot of responsibility.
#### Ground truth:
<video width="320" height="140" controls>
  <source src="zeroshot\sample3\gt.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
<table border="1">
  <tr>
    <td>
      <audio controls>
        <source src="zeroshot\sample3\s2-lgbs7p.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #1</figcaption>
    </td>
    <td>
      <audio controls>
        <source src="zeroshot\sample3\s7-lwwszp.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #2</figcaption>
    </td>
    <td>
      <audio controls>
        <source src="zeroshot\sample3\s19-swwn7a.wav" type="audio/mpeg">
        Your browser does not support the audio element.
      </audio>
      <figcaption>Reference Audio From GRID benchmark #3</figcaption>
    </td>
  </tr>
  <tr>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample3\s2.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample3\s7.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
    <td>
      <video width="320" height="140" controls>
        <source src="zeroshot\sample3\s19.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </td>
  </tr>
</table>
