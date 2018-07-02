import matplotlib.pyplot as plt
#Definir variables
r= float(input("Ingrese radio: ")) #Radio de la bola1
p0=10 #Posición inicial
v0=0 #Velocidad inicial
t0=float(input("Ingrese tiempo: ")) #Tiempo inicial
g=-9.8  #aceleración de la gravedad
dt=1
T=int(input("Ingrese Tiempo total de la simulación: ") ) #Tiempo total de la simulación
#Definir listas
posiciones=[p0]
velocidades=[v0]
tiempos=[t0]
for i in range(T):
    v0=v0+(g*dt)
    velocidades.append(v0)
    p0=p0+(v0*dt)
    posiciones.append(p0)
    t0=t0+dt
    tiempos.append(t0)
    n = int(round(T/dt))
    if p0==0:
        print(-v0)
    print(posiciones,velocidades,tiempos)
plt.plot(tiempos,posiciones)
plt.show()
