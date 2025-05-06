# ee341-lab-4-digital-filtering-and-audio-equalizer-solved
**TO GET THIS SOLUTION VISIT:** [EE341 Lab 4-Digital Filtering and Audio Equalizer Solved](https://www.ankitcodinghub.com/product/ee341-lab-4-digital-filtering-and-audio-equalizer-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;97905&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE341 Lab 4-Digital Filtering and Audio Equalizer Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column"></div>
</div>
<div class="layoutArea">
<div class="column">
&nbsp;

</div>
</div>
<div class="layoutArea">
<div class="column">
Lab Objectives

</div>
</div>
<div class="layoutArea">
<div class="column">
In this lab, we will experiment with two types of digital linear time-invariant (LTI) filters: finite impulse response (FIR) filters and infinite impulse response (IIR) filters. We will inspect the characteristics of the filters in both time and frequency domain. By completing this lab, you will gain insights into the properties of different types of digital filters and gain familiarity with the designs and implementations of them.

Part 1: Digital Filters

To start, create a new Jupyter Notebook in your ee341lab folder and name it to lab4. Import the modules: numpy, pyplot, fftpack, and simpleaudio just as you did in Lab 3. Also import the signal module from SciPy library as follows.

from scipy import signal

The signal module provides several convenient functions for creating filters and applying them to signals. It

will be our main tool for implementing filters in this lab.

Then, download microsoft_stock.txt and music.wav from Canvas and copy them to the same directory where your Jupyter Notebook is stored. We will use the signals from these files to test our filters.

Background

Every casual LTI digital filter can be described by a linear difference equation that relates the output of the filter 𝑦[𝑛] to the input of the filter 𝑥[𝑛]:

𝑁𝑀

∑ 𝑎𝑘𝑦[𝑛 − 𝑘] = ∑ 𝑏𝑘𝑥[𝑛 − 𝑘] 𝑘=0 𝑘=0

The time-domain difference equation presented above is equivalent to the frequency-domain transfer function:

</div>
</div>
<div class="layoutArea">
<div class="column">
Developed/revised by Kevin Lin, Yibo Cao, and Tai Chen 2019

</div>
</div>
<div class="layoutArea">
<div class="column">
𝐻(𝑧)=

</div>
<div class="column">
𝑌(𝑧) 𝑋(𝑧)

</div>
<div class="column">
∑𝑀 𝑏 𝑧−𝑘

= 𝑘=0 𝑘 𝑤h𝑒𝑟𝑒𝑧=𝑒𝑗ω

</div>
</div>
<div class="layoutArea">
<div class="column">
∑𝑁 𝑎 𝑧−𝑘 𝑘=0 𝑘

</div>
</div>
<div class="layoutArea">
<div class="column">
In the equation, 𝑎𝑘 and 𝑏𝑘 are the filter coefficients. 𝑎𝑘 is an array of length 𝑁 + 1 and 𝑏𝑘 is an array of length 𝑀 + 1. The length of the filter, also called the number of taps, is the maximum of the lengths of the two coefficient arrays, i.e. max(𝑁, 𝑀) + 1. The order of the filter is the length of the filter minus 1, i.e. max(N, M).

By rearranging the equation, we can isolate the current output 𝑦[𝑛] to the left-hand side: 1𝑀𝑁

𝑦[𝑛]=𝑎 (∑𝑏𝑘𝑥[𝑛−𝑘]−∑𝑎𝑘𝑦[𝑛−𝑘]) 0 𝑘=0 𝑘=1

</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
This gives us the formula for calculating the current output of the filter from the current input, past inputs and past outputs of the filter. The leading denominator coefficient 𝑎0 is usually set to 1, since the effect of a non-unit 𝑎0 is equivalent to dividing all other coefficients by 𝑎0.

In Python, LTI digital filters can be implemented using the lfilter function from the signal module: y = signal.lfilter(b, a, x)

In the example code above, x is the input signal, y is the output signal, and a and b are the filter coefficients. All of these 4 are stored as 1D ndarrays.

Types of Filters

Filters can be classified by the shape of their frequency responses, which determine their applications.

<ul>
<li> &nbsp;Low-pass filter removes high-frequency components of the data, allowing only frequencies lower than the cut-off frequency to pass through. It is commonly used for smoothing the data. For audio, applying low-pass filter removes high-pitched sound and upper harmonics, which results in a warm and muddy sound. For image, applying low-pass filter removes sharp details, which results in a blurred image.</li>
<li> &nbsp;High-pass filter removes low-frequency components of the data, allowing only frequencies higher than the cut-off frequency to pass through. It is commonly used for removing DC component from the signal and for extracting details from the data. For audio, applying high-pass filter removes the bass component, which results in a sharp and crispy sound.</li>
<li> &nbsp;Band-pass filter allows only a certain range of frequency to pass through. It is usually used in communication systems, such as radio, to select a channel. Multiple band-pass filters can also form an equalizer which offers detailed control of the level of each band.</li>
<li> &nbsp;Band-reject filter removes a certain range of frequency. It is usually used to remove a specific unwanted frequency from the signal, e.g. removing the feedback of a loudspeaker.</li>
<li> &nbsp;All-pass filter lets all frequency components equally pass through. However, it applies different amount of phase-shift (delay) to different frequency, which is useful for some applications.
FIR Filter

LTI digital filters can also be classified into two types by structure: finite impulse response (FIR) filter, and infinite impulse response (IIR) filter. A FIR filter is a filter with no denominator coefficients 𝑎𝑘, except for 𝑎0, which we set to 1. Therefore, by definition, the output of a FIR filter can be expressed as:

𝑀

𝑦[𝑛] = ∑ 𝑏𝑘𝑥[𝑛 − 𝑘] 𝑘=0

Shown by the equation, the output of a FIR filter is simply a weighted average of the current and past inputs, with the weights being the nominator coefficients 𝑏𝑘. For this reason, people also call it as the moving average filter. Also notice that the equation exactly describes the convolution operation: 𝑦[𝑛] = 𝑏[𝑛] ⊛ 𝑥[𝑛], with the impulse response being the nominator coefficients 𝑏𝑘. Because there can only be a finite number of nominator coefficients, the length of the impulse response is also finite; hence the name “finite impulse response”.
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column"></div>
</div>
<div class="layoutArea">
<div class="column">
&nbsp;

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
EE 341 Lab 4 Since the impulse response has finite length, you can implement the filter by directly computing the convolution

instead of using signal.lfilter. To calculate convolution, use signal.convolve as follows: y = signal.convolve(x, h)

where h is the impulse response of the filter, stored as a 1D ndarray. The advantage of convolve is that it can leverage the circular convolution theorem to use FFT to speed-up the calculation.

Task 1: Implement a Moving Average Filter

Load the data in signal_data.txt to an ndarray using the following statement: data = np.genfromtxt(‘signal_data.txt’)

The data is a 100-second sinusoidal signal with random noise. Plot the data. Notice the quick changes in the data which correspond to the high frequency component. People tend to remove the noise by using a moving average filter. Consider the following 30-second moving average filter:

𝑦[𝑛]= 1 (𝑥[𝑛]+𝑥[𝑛−1]+⋯+𝑥[𝑛−29]) 30

which corresponds to the impulse response:

h[𝑛] = 1 (𝑢[𝑛] − 𝑢[𝑛 − 30]) 30

Apply this filter to the 100-second signal using both lfilter and convolve. For each the two implementations, plot the original data and the filtered data in the same plot. Does the filtered result look smoother? Plot the magnitude of the frequency response of the filter to verify that this system corresponds to a low-pass filter.

In your notebook, include the plot for the lfilter implementation, the plot for the convolve implementation and the plot of the system frequency response. Be sure to label the axes and give each plot a meaningful title. Explain the differences in the results of the two implementations. How would you adjust the implementations so that they give identical results?

IIR Filter

We already know that FIR filters don’t have any denominator coefficients 𝑎𝑘 for 𝑘 ≥ 1. IIR filters, in contrast, have some non-trivial denominator coefficients. Therefore, by definition, the output of an IIR filter can be expressed as:

𝑀𝑁

𝑦[𝑛] = ∑ 𝑏𝑘𝑥[𝑛 − 𝑘] − ∑ 𝑎𝑘𝑦[𝑛 − 𝑘] 𝑘=0 𝑘=1

As shown by the equation, the output of an IIR filter is the weighted average of not only the current and past inputs, but also past outputs. Since the current value of 𝑦 depends on the previous values of 𝑦, IIR filter is also known as the recursive filter. Because of the recursion, the impulse response of a stable IIR filter decays over time but never dies off, making it infinite length, and hence the name “infinite impulse response”.

Apart from the length of the impulse response, FIR and IIR have many other different properties as listed below.

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
<ul>
<li> &nbsp;Order: FIR filters require a large filter order to meet the requirements of passband, stopband, ripple, and roll-off. In contrast, IIR filters can accomplish them with a lower order. Therefore, FIR filters are computationally more expensive compared to IIR filters.</li>
<li> &nbsp;Frequency Response: The frequency response of a FIR filter has ripples in both passband and stopband and has a slow roll-off at the cut-off frequency. In contrast, the frequency response of an IIR filter is much smoother and has sharper roll-off at the cut-off frequency.
 Stableness: The poles of a FIR filter can only be at the origin, so it must be stable. In contrast, the poles of an IIR filter can be anywhere, so it can be either stable or unstable.

 Phase: FIR filters can be designed to have a linear phase which preserves the shape of the waveform. In contrast, IIR filters have non-linear components in the phase response that can distort the shape of the waveform.

Using Classic Filter Designs

Instead of designing filters by ourselves, we can use some classic filter designs provided by the SciPy package. For IIR filter, we can use the Butterworth design, which is a design that has no ripple in the frequency response. To create a Butterworth filter, use the signal.butter function:1

b, a = signal.butter(order, W, type)

where b and a are the filter coefficients, order is the order of the filter, freq is the cutoff frequency and type can be either ’lowpass’ or ’highpass’. The unit of W is the normalized frequency, which has the range 0 ≤ 𝑊 ≤ 1 where 1 corresponds to the Nyquist frequency (half of the sampling rate). This range also maps to the DTFT or DFT range: 0 ≤ ω ≤ π or 0 ≤ 𝑓 ≤ 0.5 we used in Lab 3.

For FIR filter, we can use the window-method design, which approximates the impulse response of an ideal filter. To create a window-method filter, use the signal.firwin function:

where b is the numerator coefficient or impulse response, num_taps is the length of the filter and W is the cutoff frequency which has the unit of the normalized frequency.

Task 2: Analyze the Characteristics of Filters

For this task, you will use the analyze function provided in Appendix A to analyze the characteristics of 4 different filters. In particular, we will look at how FIR and IIR filters behave differently in terms of frequency response, impulse response and poles / zeros.

To start, copy the analyze function in Appendix A to a new code cell and execute it. Then, implement the 4 following filters. Each filter should have an order of 10 and a cutoff frequency of ω = 0.1𝜋.

<ul>
<li> &nbsp;Low-pass IIR filter using Butterworth design.</li>
<li> &nbsp;Low-Pass FIR filter using window-method design.
1 The Butterworth filter is actually an analog (continuous-time) filter, so the digital IIR version is only approximated.
</li>
</ul>
</li>
</ul>
</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
# Lowpass:

b = signal.firwin(num_taps, W)

# Highpass:

b = signal.firwin(num_taps, W, pass_zero = False)

</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
<ul>
<li> &nbsp;High-pass IIR filter using Butterworth design.</li>
<li> &nbsp;High-pass IIR filter using window-method design.
Then for each filter, apply the analyze function, which will produce plots of the frequency response, impulse response and poles / zeros.

Finally, apply each filter to the each of the following signals:
</li>
</ul>
<ul>
<li> &nbsp;The data in microsoft_stock.txt, which is the daily stock price of Microsoft over 4 years.</li>
<li> &nbsp;A pulse of length 20:
𝑥[𝑛] = 𝑢[𝑛] − 𝑢[𝑛 − 20] where 𝑥[𝑛] is of total length 60 (so append 40 zeros to the end).

In your notebook, include the 4 plots produced by the analyze function, and for each input signal, plot the original signal and the output of each filter in the same set of axes. Comment on the differences in the frequency response of the two filters (magnitude and phase) and how this impacts the outputs. When commenting on frequency responses, consider how close the filter matches an ideal filter.

Part II: Audio Equalizer

In this section, you will implement an audio equalizer using three different filters. Equalizer works by first breaking down the audio signal into multiple frequency bands using filters. Each band will then receive a different gain. Finally, all bands are summed together to produce the output signal. Audio mixing boards do exactly this, though with many more bands than the three bands we have here. The term “equalizer” comes from the fact that people often want to boost the gain of low-energy frequency ranges of the sound or to reduce the gain of high-energy frequency ranges of the sound. By doing so, each frequency range of the sound will have about equal loudness, allowing them to mix together nicely.

Shown below is the signal flow diagram of the 3-band equalizer you will implement. 𝐺1, 𝐺2 and 𝐺3 are correspondingly the gains of the bass, mid and treble frequency ranges. The coefficients of each filter are provided in Table 1. However, you need to figure out by yourself which filter does each set of coefficients correspond to. The magnitude response of each filter is shown in Figure 2.
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
EE 341 Lab 4

</div>
</div>
<div class="layoutArea">
<div class="column">
Developed/revised by Kevin Lin, Yibo Cao, and Tai Chen 2019

</div>
</div>
<div class="layoutArea">
<div class="column">
Figure 1: Signal flow of the equalizer

</div>
</div>
<div class="layoutArea">
<div class="column">
5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
Table 1: Filter coefficients of the equalizer

Filter Coefficients Which filter? (LP, HP or BP?)

</div>
</div>
<div class="layoutArea">
<div class="column">
EE 341 Lab 4

</div>
</div>
<table>
<tbody>
<tr>
<td>
<div class="layoutArea">
<div class="column">
b1 = [11.713, 0, -23.4257, 0, 11.713]

a1 = [1800, -6656.7, 9341, -5896.1, 1413.4]

</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
b2 = [0.2982, 0.89471, 0.89471, 0.2982] a2 = [1800, -4989.8, 4625.2, -1433]

</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
b3 = [688.1, -2752.5, 4128.71, -2752.47, 688.12] a3 = [1000, -3256.6, 4033.77, -2246, 473.51]

</div>
</div>
</td>
</tr>
</tbody>
</table>
<div class="layoutArea">
<div class="column">
Figure 2: Magnitude response of the equalizer

Task 3: Implement the 3-Band Equalizer

First, identify which filter does each set of coefficients in Table 1 correspond to. Then, implement the equalizer by writing a function that takes a sound signal and the gain terms 𝐺1, 𝐺2 and 𝐺3 as inputs, applies the filters, multiplies the filter outputs by the gain terms, and sums the results. The gain terms supplied to the function should be in decibels (dB).

After you implemented your equalizer, load the sound file music.wav using the function provided in Appendix B (the same one you used in Lab 3). Apply the equalizer to the music with 𝐺1 = 𝐺2 = 𝐺3 = 0 𝑑𝐵 and play the output. Verify that it sounds the same as the original input. Then, experiment with different sets of gains (for example 𝐺1 = 𝐺2 = 0 𝑑𝐵 and 𝐺3 = −40 𝑑𝐵, or 𝐺1 = −40 𝑑𝐵 and 𝐺2 = 𝐺3 = 0 𝑑𝐵). Discuss how the filtered sound sounds different in at least two different cases.

To play sound, use the function below.

In your notebook, include your answers to the blanks in Table 1, the code of your equalizer function and the code of playing the outputs of the equalizer. Discuss how the filtered sound sounds different under different sets of gains.

Developed/revised by Kevin Lin, Yibo Cao, and Tai Chen 2019

</div>
</div>
<div class="layoutArea">
<div class="column">
def play(samples, sample_rate):

sa.play_buffer((np.clip(samples, -1, 1) * 32767).astype(‘int16’),

1, 2, sample_rate).wait_done()

</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
Lab Submission Requirements

Submit your completed Jupyter Notebook in the ipynb format to Canvas. The notebook file can be obtained by clicking the menu: File – Download as – Notebook or directly accessed from the ee341lab folder in your home directory. Make sure to include the code of all the 3 tasks in code cells and include the required discussions of each task in text cells.

Appendix A: Filter Analysis Function

</div>
</div>
<div class="layoutArea">
<div class="column">
EE 341 Lab 4

</div>
</div>
<div class="layoutArea">
<div class="column">
Copy the function below to a code cell and execute it. To apply it to a filter, call analyze(b, a, title) where b and a are the filter coefficients and title is the title of the plots.

</div>
</div>
<table>
<tbody>
<tr>
<td>
<div class="layoutArea">
<div class="column">
def analyze(b, a, title):

</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
b = np.reshape(b, -1)

a = np.reshape(a, -1)

fig = plt.figure(figsize = (10, 8)) fig.suptitle(title, fontsize = ‘x-large’) fig.subplots_adjust(hspace = 0.5, wspace = 0.3)

<pre># Plot frequency response
</pre>
w, h = signal.freqz(b, a, 1024)

w_majors = np.array([0, 0.2, 0.4, 0.6, 0.8, 1]) * np.pi w_labels = [‘0′, r’$0.2\pi$’, r’$0.4\pi$’,

r’$0.6\pi$’, r’$0.8\pi$’, r’$\pi$’] ax = fig.add_subplot(221)

ax.plot(w, 20 * np.log10(np.abs(h))) ax.set_xticks(w_majors) ax.set_xticklabels(w_labels) ax.set_title(‘Magnitude Response’) ax.set_xlabel(‘Frequency [rad]’) ax.set_ylabel(‘Gain [dB]’)

ax = fig.add_subplot(222)

ax.plot(w, np.rad2deg(np.unwrap(np.angle(h)))) ax.set_xticks(w_majors) ax.set_xticklabels(w_labels) ax.set_title(‘Phase Response’) ax.set_xlabel(‘Frequency [rad]’) ax.set_ylabel(‘Phase [deg]’)

<pre># Plot impulse response
</pre>
x = np.zeros(50); x[0] = 1 y = signal.lfilter(b, a, x) ax = fig.add_subplot(223)

</div>
</div>
</td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
ax.stem(np.arange(len(y)), y) ax.set_title(‘Impulse Response’) ax.set_xlabel(‘Time’) ax.set_ylabel(‘Output’)

<pre># Plot poles &amp; zeros
</pre>
n_taps = max(len(b), len(a))

b = np.pad(b, (0, n_taps – len(b)), ‘constant’) a = np.pad(a, (0, n_taps – len(a)), ‘constant’) z, p, k = signal.tf2zpk(b, a)

</div>
</div>
</td>
</tr>
</tbody>
</table>
</div>
<div class="page" title="Page 8">
<div class="section">
<div class="layoutArea">
<div class="column">
ax = fig.add_subplot(224, projection = ‘polar’) ax.plot(np.angle(p), np.abs(p), ‘x’)

ax.plot(np.angle(z), np.abs(z), ‘o’, markerfacecolor = ‘none’) lines, labels = ax.set_rgrids([1])

for line in lines: line.set_color(‘black’) ax.set_thetagrids([0, 90, 180, 270], [‘Re(z)’, ‘Im(z)’]) ax.set_rlabel_position(0) ax.spines[‘polar’].set_visible(False) ax.set_title(‘Poles &amp; Zeros’, y = 1.1)

</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
Appendix B: Loading WAV Files

To load sound data from WAV files into your Python program, firstly copy the files you want to load into the same directory where your Jupyter Notebook is stored (that is the ee341lab folder in your home directory if you followed our convention in Lab 1). Then, add the following import statement after your other imports:

import scipy.io.wavfile as wav

Ideally, you should be able to directly use wav.read from this package to load files. However, WAV files can have different quantization formats and number of channels that will cause troubles later on. Therefore, we provide you the following helper function to help you deal with different formats.

</div>
</div>
<div class="section">
<div class="layoutArea">
<div class="column">
# Load a WAV file.

# Return the sampling rate and the sample array. def wav_load(file_name):

<pre>  # Load the raw data.
</pre>
sr, data = wav.read(file_name) # Only use the first channel. if data.ndim &gt; 1:

data = data[:, 0]

# Convert to float32 quantization. kind = data.dtype.kind

bits = data.dtype.itemsize * 8 data = data.astype(‘float32’)

if kind == ‘i’ or kind == ‘u’:

data = data / 2 ** (bits – 1) if kind == ‘u’:

data = data – 1 return sr, data

</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
Example usage:

sr, samples = wav_load(“do.wav”)

This will load the file do.wav, putting the sampling rate into the variable sr and putting the sample array into

the variable samples.

</div>
</div>
</div>
