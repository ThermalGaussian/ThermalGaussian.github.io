## THERMALGAUSSIAN :THERMAL 3D GAUSSIAN SPLATTING

![alt text](pipline.png)


## Abstract
Thermography is especially valuable for the military and other users of surveillance cameras. Some recent methods based on Neural Radiance Fields (NeRF) are
proposed to reconstruct the thermal scenes in 3D from a set of thermal and RGB images. However, unlike NeRF, 3D Gaussian splatting (3DGS) prevails due to its
rapid training and real-time rendering. In this work, we propose ThermalGaussian, the first thermal 3DGS approach capable of rendering high-quality images in
RGB and thermal modalities. We first calibrate the RGB camera and the thermal camera to ensure that both modalities are accurately aligned. Subsequently, we use the registered images to learn the multimodal 3D Gaussians. To prevent the overfitting of any single modality, we introduce several multimodal regularization
constraints. We also develop smoothing constraints tailored to the physical characteristics of the thermal modality. Besides, we contribute a real-world dataset
named RGBT-Scenes, captured by a hand-hold thermal-infrared camera, facilitating future research on thermal scene reconstruction. We conduct comprehensive experiments to show that ThermalGaussian achieves photorealistic rendering of thermal images and improves the rendering quality of RGB images. With the proposed multimodal regularization constraints, we also reduced the model’s storage cost by 90%. The code and dataset will be released.


### RGBT-Scenes Dataset
The following 10 scenes were selected for both qualitative and quantitative analysis in our paper.
<table>
        <colgroup>
                <col style="width: 12%;">
                <col style="width: 22%;">
                <col style="width: 22%;">
                <col style="width: 22%;">
                <col style="width: 10%;"> 
                <col style="width: 12%;"> 
        </colgroup>
        <caption>Each scene in the RGBT-Scenes dataset is displayed</caption>
        <thead>
            <tr>
                <th>Scene</th>
                <th>RGB</th>
                <th>Thermal</th>
                <th>MSX</th>
                <th>Views</th>
                <th class="temperature">Temp. Range</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>Dimsum</strong></td>
                <td><img src="dataset/dimsum_rgb.jpg" alt="Dimsum RGB" width="160px" height="120px"></td>
                <td><img src="dataset/dimsum_thermal.jpg" alt="Dimsum Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/dimsum_msx.jpg" alt="Dimsum MSX" width="160px" height="120px"></td>
                <td>135(train) 19(test)</td>
                <td class="temperature">23.1°C - 60.0°C</td>
            </tr>
            <tr>
                <td><strong>Daily Stuff</strong></td>
                <td><img src="dataset/DailyStuff_rgb.jpg" alt="Daily Stuff RGB" width="160px" height="120px"></td>
                <td><img src="dataset/DailyStuff_thermal.jpg" alt="Daily Stuff Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/DailyStuff_msx.jpg" alt="Daily Stuff MSX" width="160px" height="120px"></td>
                <td>78(train) 11(test)</td>
                <td class="temperature">17.5°C - 56.3°C</td>
            </tr>
            <tr>
                <td><strong>Electric Bicycle</strong></td>
                <td><img src="dataset/electromobile_rgb.jpg" alt="Electric Bicycle RGB" width="160px" height="120px"></td>
                <td><img src="dataset/electromobile_thermal.jpg" alt="Electric Bicycle Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/electromobile_msx.jpg" alt="Electric Bicycle MSX" width="160px" height="120px"></td>
                <td>42(train) 6(test)</td>
                <td class="temperature">14.5°C - 18.5°C</td>
            </tr>
            <tr>
                <td><strong>Roadblock</strong></td>
                <td><img src="dataset/roadblock_rgb.jpg" alt="Roadblock RGB" width="160px" height="120px"></td>
                <td><img src="dataset/roadblock_thermal.jpg" alt="Roadblock Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/roadblock_msx.jpg" alt="Roadblock MSX" width="160px" height="120px"></td>
                <td>32(train) 4(test)</td>
                <td class="temperature">31.0°C - 43.0°C</td>
            </tr>
            <tr>
                <td><strong>Truck</strong></td>
                <td><img src="dataset/residue_truck_rgb.jpg" alt="Truck RGB" width="160px" height="120px"></td>
                <td><img src="dataset/residue_truck_thermal.jpg" alt="Truck Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/residue_truck_msx.jpg" alt="Truck MSX" width="160px" height="120px"></td>
                <td>64(train) 9(test)</td>
                <td class="temperature">30.6°C - 249.0°C</td>
            </tr>
            <tr>
                <td><strong>Rotary Kiln</strong></td>
                <td><img src="dataset/Rotary_Kiln_rgb.jpg" alt="Rotary Kiln RGB" width="160px" height="120px"></td>
                <td><img src="dataset/Rotary_Kiln_thermal.jpg" alt="Rotary Kiln Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/Rotary_Kiln_msx.jpg" alt="Rotary Kiln MSX" width="160px" height="120px"></td>
                <td>93(train) 13(test)</td>
                <td class="temperature">5.0°C - 60.4°C</td>
            </tr>
            <tr>
                <td><strong>Building</strong></td>
                <td><img src="dataset/building_rgb.jpg" alt="Building RGB" width="160px" height="120px"></td>
                <td><img src="dataset/building_thermal.jpg" alt="Building Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/building_msx.jpg" alt="Building MSX" width="160px" height="120px"></td>
                <td>239(train) 34(test)</td>
                <td class="temperature">15.0°C - 24.0°C</td>
            </tr>
            <tr>
                <td><strong>Iron ingot</strong></td>
                <td><img src="dataset/iron_ingot_rgb.jpg" alt="Iron ingot RGB" width="160px" height="120px"></td>
                <td><img src="dataset/iron_ingot_thermal.jpg" alt="Iron ingot Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/iron_ingot_msx.jpg" alt="Iron ingot MSX" width="160px" height="120px"></td>
                <td>54(train) 7(test)</td>
                <td class="temperature">38.0°C - 350.0°C</td>
            </tr>
            <tr>
                <td><strong>Parterre</strong></td>
                <td><img src="dataset/Parterre_msx.jpg" alt="Parterre RGB" width="160px" height="120px"></td>
                <td><img src="dataset/Parterre_thermal.jpg" alt="Parterre Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/Parterre_msx.jpg" alt="Parterre MSX" width="160px" height="120px"></td>
                <td>63(train) 9(test)</td>
                <td class="temperature">18.0°C - 27.0°C</td>
            </tr>
            <tr>
                <td><strong>Landscape</strong></td>
                <td><img src="dataset/landscape_rgb.jpg" alt="Landscape RGB" width="160px" height="120px"></td>
                <td><img src="dataset/landscape_thermal.jpg" alt="Landscape Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/landscape_msx.jpg" alt="Landscape MSX" width="160px" height="120px"></td>
                <td>90(train) 13(test)</td>
                <td class="temperature">16.0°C - 23.0°C</td>
            </tr>
        </tbody>
</table>
    



### RGBT-Scenes-extend-Dataset
<table>
        <colgroup>
                <col style="width: 12%;">
                <col style="width: 22%;">
                <col style="width: 22%;">
                <col style="width: 22%;">
                <col style="width: 10%;"> 
                <col style="width: 12%;"> 
        </colgroup>
        <caption>Each scene in the expanded RGBT-Scenes dataset is displayed</caption>
        <thead>
            <tr>
                <th>Scene</th>
                <th>RGB</th>
                <th>Thermal</th>
                <th>MSX</th>
                <th>Views</th>
                <th class="temperature">Temp. Range</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><strong>Glass Cup</strong></td>
                <td><img src="dataset/Cup_rgb.jpg" alt="Dimsum RGB" width="160px" height="120px"></td>
                <td><img src="dataset/Cup_thermal.jpg" alt="Dimsum Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/Cup_msx.jpg" alt="Dimsum MSX" width="160px" height="120px"></td>
                <td>123(train) 18(test)</td>
                <td class="temperature">17.0°C - 36.6°C</td>
            </tr>
            <tr>
                <td><strong>\Transmission Tower</strong></td>
                <td><img src="dataset/Tower_rgb.jpg" alt="Daily Stuff RGB" width="160px" height="120px"></td>
                <td><img src="dataset/Tower_thermal.jpg" alt="Daily Stuff Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/Tower_msx.jpg" alt="Daily Stuff MSX" width="160px" height="120px"></td>
                <td>154(train) 23(test)</td>
                <td class="temperature">23.7°C - 26.4°C</td>
            </tr>
            <tr>
                <td><strong>Dark Scene</strong></td>
                <td><img src="dataset/Dark_rgb.jpg" alt="Electric Bicycle RGB" width="160px" height="120px"></td>
                <td><img src="dataset/Dark_thermal.jpg" alt="Electric Bicycle Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/Dark_msx.jpg" alt="Electric Bicycle MSX" width="160px" height="120px"></td>
                <td>75(train) 11(test)</td>
                <td class="temperature">17.5°C - 21.6°C</td>
            </tr>
            <tr>
                <td><strong>Plant Equipment</strong></td>
                <td><img src="dataset/Plant_rgb.jpg" alt="Roadblock RGB" width="160px" height="120px"></td>
                <td><img src="dataset/Plant_thermal.jpg" alt="Roadblock Thermal" width="160px" height="120px"></td>
                <td><img src="dataset/Plant_msx.jpg" alt="Roadblock MSX" width="160px" height="120px"></td>
                <td>192(train) 28(test)</td>
                <td class="temperature">27.8°C - 54.9°C</td>
            </tr>
        </tbody>
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
