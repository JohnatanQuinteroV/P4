# P4 
Para el problema 1 se implemento la siguiente dinámica.

 En la funcion modulador1, la portadora es, portadora = np.cos(2*np.pi*fc*t_periodo)
senal_Tx1, Pm1, portadora1, moduladora1 = modulador1(bits_Tx, fc, mpp)  #creamos señal y portadora1

 En la funcion modulador2, la portadora es, portadora = np.cos(2*np.pi*fc*t_periodo)
senal_Tx2, Pm2, portadora2, moduladora2 = modulador2(bits_Tx, fc, mpp)  #creamos señal y portadora2

Y en la sección del main, se implemento la suma de portadas y de señales. 
senal_Tx=senal_Tx1+senal_Tx2  #sumamos las señales

# 4. Se transmite la señal modulada, por un canal ruidoso
senal_Rx = canal_ruidoso(senal_Tx, Pm, SNR)

portadora = portadora1 + portadora2 #sumamos las portadoras

# 5. Se desmodula la señal recibida del canal
bits_Rx, senal_demodulada = demodulador(senal_Rx, p
