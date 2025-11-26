# Stability-Analysis-using-Polar-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=10/(S(1+0.5S)(1+0.2S)) using polar plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
~~~
num=[10]
den=[0.1 0.7 1 0]
sys=tf(num,den)
[mag,phase,W]=bode(sys)
mag=squeeze(mag)
phase=squeeze(phase)
phase1=deg2rad(phase)
polarplot(phase1,mag,'linewidth',1.5)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
~~~

## Output:
<img width="709" height="651" alt="Screenshot 2025-11-26 200406" src="https://github.com/user-attachments/assets/7edbd859-4c83-4a83-a26c-192a7ddf661d" />


## Result:
~~~
Thus the polar plot for the given transfer function was drawn and verified using MATLAB. 
Gain margin = 0.7
Phase Margin = -8.8865
Gain crossover frequency = 3.7565
Phase crossover frequency =3.1623
The system is  unstable
~~~
