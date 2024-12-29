# 🤖 Robotics Application Manager

The **🤖 Robotics Application Manager** (RAM) provides an advanced framework for integrating, configuring, and managing robotics workflows. Designed as a dynamic state machine, it facilitates smooth transitions across different application states. As part of the [🌐 JdeRobot](https://jderobot.org) ecosystem, RAM caters to a wide array of robotics and computer vision applications.

---

## 🌟 Highlights

- **🔧 Modular Framework:** Simplifies management of diverse robotics tasks.
- **💻 Multi-Platform Support:** Ensures compatibility across operating systems.
- **😊 User-Friendly:** Built for developers and researchers.
- **📈 Scalable Design:** Adapts seamlessly to projects of any size.
- **🧠 Intelligent State Management:** Automates application state transitions.

---

## 🛠️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/JdeRobot/RoboticsApplicationManager.git
cd RoboticsApplicationManager
```

### 2. Install Dependencies

```bash
pip install -r docs/requirements.txt
```

---

## 🚀 Developing a New RAM Launcher

### Steps to Build a Launcher

1. **Configure Transitions**:
   - Add entries in `launcher_visualization.py` for visualization setups or `launcher_world.py` for world configurations.

2. **Create Required Modules**:
   - Implement custom modules like `launcher_abc_module.py`.

3. **Activate the Setup**:
   - Utilize classes such as `LauncherVisualization` to execute the new configuration.

---

## 🤖 Utilizing the Dummy RAM Client

The Dummy RAM Client streamlines testing and debugging by simulating key application transitions.

### Usage Instructions

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/JdeRobot/RoboticsApplicationManager.git -b <src-branch>
   ```

2. **Run a Docker Container**:

   ```bash
   docker run --rm -it -p 7164:7164 -p 6080:6080 -p 1108:1108 -p 7163:7163 jderobot/robotics-backend
   ```

3. **Execute the Dummy Client**:

   ```bash
   cd RoboticsApplicationManager/test/
   python3 dummyclient.py
   ```

   Access the simulation at [http://127.0.0.1:6080/vnc.html](http://127.0.0.1:6080/vnc.html).

---

## 🔑 Core Functionalities

### Manager Class Highlights

- **Primary States**:
  - `idle`: Waiting for connection.
  - `connected`: Ready for communication.
  - `world_ready`: Environment configured.
  - `visualization_ready`: Visualization initialized.
  - `application_running`: Application active.
  - `paused`: Application paused.

- **State Transitions**:
  - Include `connect`, `launch_world`, `prepare_visualization`, `run_application`, `pause`, `resume`, `terminate`, `stop`, and `disconnect`.

### Key System Components

- **ManagerConsumer**: Oversees client communication and message queues.
- **LauncherWorld**: Dynamically sets up robotic environments.
- **LauncherVisualization**: Initializes visualization modules.
- **Application Process**: Manages execution flow.
- **Server Integration**: Enables live GUI-based controls.

### Essential Methods

- `on_connect`: Moves to `connected` state.
- `on_launch_world`: Sets up the robotic environment.
- `on_prepare_visualization`: Configures visualization tools.
- `on_run_application`: Starts the application.
- `on_pause` / `on_resume`: Manages pausing and resuming.
- `on_terminate`: Ends application operations.
- `on_disconnect`: Handles cleanup and disconnection tasks.

---

## 👥 Contributors

Special thanks to all contributors:

- ango1994
- ReyDoran
- javizqh
- dduro2020
- pawanw17
- OscarMrZ
- Blancasr
- Arcane-01
- espilya
- pariaspe
- dpascualhe
- jmplaza
- CDAM2020

---

## 🤝 Contributing to RAM

Want to contribute? Here's how:

1. **Fork the Repository**:

   ```bash
   git checkout -b feature/your-feature
   ```

2. **Commit Your Changes**:

   ```bash
   git commit -m "✨ Add feature description"
   ```

3. **Push to Your Branch**:

   ```bash
   git push origin feature/your-feature
   ```

4. **Submit a Pull Request**:
   - Open a PR for review and integration.

---

## 📜 License

This project is licensed under the [📜 GPL v3 License](LICENSE).

---

## 📬 Get in Touch

Have questions or feedback? Contact us via the [🌐 JdeRobot Team](https://jderobot.org/Contact) or submit issues directly on the repository.

---

Thank you for choosing RAM! 🚀 Happy Building! 💻

