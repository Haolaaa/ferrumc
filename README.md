<img style="width: 100%" src="https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/header.svg?raw=true" alt="FerrumC Header">
<div align="center">
    <img src="https://img.shields.io/github/license/Sweattypalms/ferrumc?style=for-the-badge&color=red" alt="License">
    <img src="https://img.shields.io/github/languages/code-size/Sweattypalms/ferrumc?style=for-the-badge&color=red" alt="Code Size">
    <img src="https://www.aschey.tech/tokei/github.com/Sweattypalms/ferrumc?style=for-the-badge&color=red" alt="Lines of Code">
    <img src="https://img.shields.io/badge/language-Rust-orange?style=for-the-badge&color=red" alt="Language">
</div>
<p align="center">
  <a href="https://discord.gg/qT5J8EMjwk">
    <img src="https://img.shields.io/discord/1277314213878173726?color=7289DA&label=Join%20our%20Discord&logo=discord&logoColor=white" alt="Join our Discord&style=for-the-badge">
  </a>
</p>

## 📖 About

FerrumC is a Minecraft server implementation written from the ground up in Rust. Leveraging the power of the Rust
programming language, it achieves high performance and low latency as well as amazing memory efficiency!

<img src="https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/in_game.png?raw=true" alt="In-game screenshot">


<h1>✨ Key Features</h1>

<ul>
   <li>
     <h4>Customizable server list</h4>
     <img src="https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/server%20list.png?raw=true" alt="Server list">
   </li>
   <li>
     <h4>Extremely fast and adaptable update speeds</h4>
     <img src="https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/mind%20boggling.gif?raw=true" alt="Mind boggling">
   </li>
   <li>
     <h4>Highly efficient memory usage</h4>
     <img src="https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/mem_use.png?raw=true" alt="Low memory usage">
   </li>
   <li>
     <h4>Customizable configuration</h4>
     <img src="https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/config.png?raw=true" alt="Configuration">
   </li>
   <li>
      <h4>🔄 Can import existing worlds from vanilla minecraft</h4>
   </li>
   <li>
      <h4>🌐 Compatible with vanilla Minecraft clients (Currently only 1.20.1)</h4>
   </li>
   <li>
      <h4>🛠 Open-source for community contributions and customization</h4>
   </li>
   <li>
      <h4>⚡ Built with Rust for memory safety and concurrency</h4>
   </li>
</ul>

## 🎯 Current Features and Roadmap

<details open>
<summary><b>✅ Implemented Features</b></summary>

- Player connection and authentication

![Player Joining](https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/player_joining.png?raw=true)

- Entity Component System

![ECS Diagram](https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/ECSBlockDiagram.png)
 
*Entity Component System, unlike inheritance-based systems,
is data-oriented and allows for better performance and scalability.*

- Packet handling, serialization, and deserialization

*Incoming packet definition*

![Incoming packet definition](https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/packet.png?raw=true)

*Packet handling*

![Packet handling](https://github.com/Sweattypalms/ferrumc/blob/dev/README/assets/packet_handling.png?raw=true)

- Great logging system

```log
// [Timestamp (stripped)] [Log Level] [System Name] [Connection?] [Module (rm'd for brevity)]: [Message]
2024-08...Z DEBUG sys{name=ConnectionHandler}:conn{addy=127.0.0.1:59996}: Sweattypalms moved to (0,400,0)
2024-08...Z DEBUG sys{name=ChunkSender}: Sending chunks to player: Sweattypalms @ (0,400,0)
2024-08...Z DEBUG sys{name=TickSystem}: Ticked `Sweattypalms`
```

- Keep-alive system
- NBT serialization and deserialization

</details>


<details>
<summary><b>🔨 In Progress</b></summary>

- World stuff (chunks loading, saving, etc.)
- Database integration (embedded)
- Entities and physics

</details>

<details>
<summary><b>📅 Planned Features</b></summary>

- Chat system
- Advanced world generation
- Plugin support + API (Rust and Lua)
- Multi-world support
- Performance optimizations

</details>

## 🚀 Getting Started

### Prerequisites

- Rust compiler (latest nightly version)
- Cargo (comes with Rust)

### 📥 Installation

[//]: # (#### Option 1: Download pre-compiled binary &#40;Maybe outdated!&#41;)

[//]: # ()

[//]: # (1. Go to the [Releases]&#40;https://github.com/Sweattypalms/ferrumc/releases&#41; page)

[//]: # (2. Download the latest version for your operating system)

[//]: # (3. Extract the archive to your desired location)

<p>
Unfortunately, the server is not yet ready for production use. If you want to try it out, you can compile it from source.
</p>

#### Compile from source (Bleeding edge updates, always up-to-date)

```bash
# Clone the repository
git clone https://github.com/Sweattypalms/ferrumc
cd ferrumc

# Build the project
cargo build --release
```

### The binary will be in target/release/

### 🖥️ Usage

1. Move the FerrumC binary to your desired server directory
2. Open a terminal in that directory
3. Run the server:
    - Windows: `./ferrumc.exe`
    - Linux/macOS: `./ferrumc`
4. (Optional) Generate a config file: `./ferrumc --setup`
5. Edit the generated `config.toml` file to customize your server settings

## 🛠️ Development

We welcome contributions! If you'd like to contribute to FerrumC, please follow these steps:

1. Fork the repository
2. Create a new branch for your feature
3. Implement your changes
4. Write or update tests as necessary
5. Submit a pull request

Join our [Discord server](https://discord.gg/qT5J8EMjwk) to get help or discuss the project!

## 📜 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🙏 Acknowledgments

- [wiki.vg](https://wiki.vg): Used for protocol documentation
- [Tokio Runtime](https://github.com/tokio-rs/tokio): Asynchronous runtime for Rust
- [Valence](https://github.com/valence-rs/valence): VarInt/VarLong encoding and decoding
- [Unity](https://docs.unity3d.com/Packages/com.unity.entities@0.1/manual/ecs_core.html): ECS Diagram
