# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.
## Theory:
![WhatsApp Image 2025-11-27 at 23 38 29_f8c168f9](https://github.com/user-attachments/assets/a79bddab-db1f-4411-b130-44b1370dddc9)
![WhatsApp Image 2025-11-27 at 23 38 29_43f5cee6](https://github.com/user-attachments/assets/5d628a0c-d110-43b8-8385-68b57875bd24)
![WhatsApp Image 2025-11-27 at 23 38 29_2469266a](https://github.com/user-attachments/assets/86492b97-9238-4cd1-beef-33fee522d647)



## Program: 
num=1
den=[0.05 0.56 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end

## Output:
<img width="707" height="630" alt="image" src="https://github.com/user-attachments/assets/24022199-283d-4d03-b717-c2ab7217f31b" />

## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12<br>
Phase Margin = 60 <br>
Gain crossover frequency = 0.907 <br>
Phase crossover frequency = 4.4721<br>
The system is stable
