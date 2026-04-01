Aim

To implement and analyze phase modulation (PM) using SCILAb

Apparatus Required

 Labtop
 Scilab Software 

 Theory
Phase Modulation (PM) is a technique where the phase of the carrier wave is varied in proportion to the instantaneous amplitude of the input signal (message signal). Unlike frequency modulation, where the frequency is varied, in phase modulation, the phase angle of the carrier wave changes with the amplitude of the message signal.

Program
```
Am=5.4;
Ac=10.8;
fm=416;
fc=4160;
fs=41600;
t=0:1/fs:2/fm;
beta=4.5;

em=Am*cos(2*3.14*fm*t);
subplot(4,1,1);
plot(t,em);

ec=Ac*cos(2*3.14*fc*t);
subplot(4,1,2);
plot(t,ec);

efm=Ac*cos((2*3.14*fc*t)+beta*sin(2*3.14*fm*t));
subplot(4,1,3);
plot(t,efm);

epm=Ac*cos((2*3.14*fc*t)+beta*cos(2*3.14*fm*t));
subplot(4,1,4);
plot(t,epm);

```
Waveform
<img width="1901" height="1088" alt="image" src="https://github.com/user-attachments/assets/5dcd5188-4c7b-4bee-8fe9-e14c70d844e4" />

waveform
<img width="1600" height="936" alt="image" src="https://github.com/user-attachments/assets/7749fa67-5e36-43c0-9568-8a242b349e32" />

Result

The message signal, carrier signal, and phase-modulated (PM) signal will be displayed in separate plots. The modulated signal will show phase variations corresponding to the amplitude of the message signal.
