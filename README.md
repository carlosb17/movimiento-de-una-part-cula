# movimiento-de-una-part-cula
python
#Definir variables
r= float(input("Ingrese radio: ")) #Radio de la bola
p0=float(input("Ingrese posición inicial: ")) #Posición inicial
v0=float(input("Ingrese velocidad inicial: ")) #Velocidad inicial
t0=float(input("Ingrese tiempo: ")) #Tiempo inicial
g=9.8  #aceleración de la gravedad
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
    print(posiciones,velocidades,tiempos)
