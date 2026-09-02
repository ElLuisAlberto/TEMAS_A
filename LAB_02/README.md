# Laboratorio 02: Gemelo digital de un manipulador

## Objetivo

Desarrollar y visualizar el modelo digital de un manipulador robótico mediante URDF en ROS 2. El modelo define sus enlaces, articulaciones, geometrías y límites de movimiento, y se visualiza en RViz.

## Contenido

El workspace incluye dos paquetes:

- `arm_description`: modelo del manipulador de cuatro articulaciones desarrollado para el laboratorio.
- `kinova_description`: modelo del manipulador Kinova utilizado como referencia.

El paquete `arm_description` contiene:

- Cinco enlaces: `base_link`, `link_1`, `link_2`, `link_3` y `link_4`.
- Cuatro articulaciones de revolución.
- Modelos STL para representar cada componente.
- Un archivo de configuración de RViz.
- Un archivo launch para iniciar la visualización y el control de articulaciones.

## Requisitos

- Ubuntu 24.04
- ROS 2 Jazzy
- RViz 2
- `robot_state_publisher`
- `joint_state_publisher_gui`

## Compilación

Desde la carpeta del laboratorio:

```bash
cd arm_ws
source /opt/ros/jazzy/setup.bash
colcon build --symlink-install
source install/setup.bash