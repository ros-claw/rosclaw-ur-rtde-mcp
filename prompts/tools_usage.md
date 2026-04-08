# Tools Usage Guide: UR RTDE

## Connection

### `connect(ip: str, port: int = 30004)`
Connect to UR robot controller.

**Parameters**:
- `ip`: Robot controller IP address
- `port`: RTDE port (default 30004)

---

### `disconnect()`
Disconnect from robot controller.

---

## Movement

### `move_joints(positions, speed, acceleration)`
Move to joint positions.

**Parameters**:
- `positions`: List of 6 joint angles (radians)
- `speed`: Joint speed (0.0 to 3.14 rad/s)
- `acceleration`: Joint acceleration (rad/s²)

---

### `move_linear(pose, speed, acceleration)`
Linear TCP movement.

**Parameters**:
- `pose`: [x, y, z, rx, ry, rz] in meters and radians
- `speed`: TCP speed (m/s)
- `acceleration`: TCP acceleration (m/s²)

---

### `get_joint_states()`
Get current joint positions, velocities, and torques.

---

### `get_tcp_pose()`
Get current TCP pose [x, y, z, rx, ry, rz].

---

## I/O Control

### `set_digital_output(pin, value)`
Set digital output pin.

### `get_digital_input(pin)`
Read digital input pin.

---

## Gripper Control

### `open_gripper()`
Open Robotiq gripper.

### `close_gripper(force=20)`
Close gripper with specified force (Newtons).
