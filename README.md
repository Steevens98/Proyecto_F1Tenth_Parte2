# Proyecto_F1Tenth_Parte2

## Parte 1:📦 Instalación y Ejecución

### Paso 1: Clonar el repositorio

El repositorio ya está estructurado como un **workspace de ROS 2**, por lo que no se necesita crear carpetas adicionales.

```bash
cd $HOME
git clone https://github.com/Steevens98/Proyecto_F1Tenth_Parte2.git
```

https://github.com/user-attachments/assets/92f9814c-1da2-4cc1-bae1-4db4c41db77b

Estructura esperada del paquete:

```
Proyecto_F1Tenth_Parte2/   
├── src/                                                      
│   └── f1tenth_controller/                                   
│       ├── f1tenth_controller/
│       │   ├── __init__.py
│       │   ├── follow_the_gap.py
│       │   ├── lap_timer.py
│       │   ├── opponent1_follow_gap.py
│       │   └── opponent2_follow_gap.py  
│       ├── resource
│       │   └── f1tenth_controller
│       ├── test
│       │   ├── test_copyright.py
│       │   ├── test_flake8.py
│       │   └── test_pep257.py
│       ├── package.xml
│       ├── setup.cfg
│       └── setup.py
├── videos/
│    └── Ejecucion_Proyecto.mp4                                             
└── README.md          
```

### Paso 3: Compilar el paquete

```bash
cd Proyecto_F1Tenth_Parte2/
colcon build
```

https://github.com/user-attachments/assets/22c46512-4d98-441c-949f-7f7bc326c370

### Paso 4: Ejecutar el simulador y los nodos

⚠️ Nota : Tener instalado el simulador, sino instalarlo : https://github.com/widegonz/F1Tenth-Repository

En un terminal Ejecutar el Simulador 
```bash
cd ~/F1Tenth-Repository
source install/setup.bash
ros2 launch f1tenth_gym_ros gym_bridge_launch.py
```

https://github.com/user-attachments/assets/0aa19cad-11f7-4c08-88bc-b787310822e3

Lanzar los nodos en terminales separadas:

Nodo `lap_timer.py`
```bash
cd Proyecto_F1Tenth_Parte2/
source install/setup.bash
ros2 run f1tenth_controller lap_timer
```

Nodo `follow_the_gap.py`
```bash
cd Proyecto_F1Tenth_Parte2/
source install/setup.bash
ros2 run f1tenth_controller follow_the_gap
```

Nodo `opponent1_follow_gap.py`
```bash
cd Proyecto_F1Tenth_Parte2/
source install/setup.bash
ros2 run f1tenth_controller opponent1_follow_gap
```

Nodo `opponent2_follow_gap.py`
```bash
cd Proyecto_F1Tenth_Parte2/
source install/setup.bash
ros2 run f1tenth_controller opponent2_follow_gap
```

https://github.com/user-attachments/assets/827e14d1-44a4-4f2c-9c74-1294e4e3f02d

## Parte 2: Ejecucion del proyecto
