<div align="center">

# ❌ Tic Tac Toe ⭕

**A classic two-player XO game built with C# and Windows Forms**

![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Windows Forms](https://img.shields.io/badge/Windows%20Forms-0078D6?style=for-the-badge&logo=windows&logoColor=white)
![Visual Studio](https://img.shields.io/badge/Visual%20Studio-5C2D91?style=for-the-badge&logo=visualstudio&logoColor=white)
![Status](https://img.shields.io/badge/status-in%20progress-orange?style=for-the-badge)

</div>

---

## 📖 About

**XO-Game-Final** is a desktop Tic Tac Toe game for two players on the same computer. Players take turns clicking a cell on the 3×3 board; the game places an **X** or an **O** image and switches turns automatically.

It was built as a hands-on project to practice C# fundamentals and Windows Forms event-driven programming.

## 📸 Screenshots

> Add a screenshot of your game here:
>
> ```markdown
> ![Gameplay](screenshots/gameplay.png)
> ```

## ✨ Features

- 🎮 Two-player local gameplay (X vs O)
- 🔄 Automatic turn switching
- 🖼️ X and O drawn from image resources
- 🧩 One shared click handler for all 9 cells (clean, no duplicated code)
- 🏷️ Cell state stored with the `Tag` property

## 🗺️ Roadmap

- [x] 3×3 board with clickable cells
- [x] Alternating X / O turns
- [ ] Winner detection (rows, columns, diagonals)
- [ ] Draw detection
- [ ] Reset / New game button
- [ ] Score counter
- [ ] Play against the computer

## 🛠️ Built With

| Technology | Purpose |
|---|---|
| **C#** | Game logic |
| **.NET / Windows Forms** | Desktop UI |
| **Visual Studio** | IDE |
| **Git & GitHub** | Version control |

## 🚀 Getting Started

### Prerequisites

- Windows 10 or 11
- [Visual Studio](https://visualstudio.microsoft.com/) with the **.NET desktop development** workload
- [Git](https://git-scm.com/)

### Run locally

```bash
# 1. Clone the repository
git clone https://github.com/YOUR-USERNAME/XO-Game-Final.git

# 2. Open the project folder
cd XO-Game-Final
```

3. Double-click **`XO-Game-Final.sln`** to open it in Visual Studio.
4. Press **F5** (or click **Start**) to build and run.

## 🎯 How to Play

1. The game starts with **X**.
2. Click any empty cell to place your mark.
3. Players alternate turns.
4. The first player to line up **three marks** in a row, column, or diagonal wins.

## 🧠 How It Works

All nine cells are `PictureBox` controls that share a single `Click` event handler. The handler uses `sender` to find out which cell was clicked, then chooses the image based on a turn counter:

```csharp
private void pictureBox1_Click(object sender, EventArgs e)
{
    PictureBox pb = (PictureBox)sender;

    if (NumberChoise % 2 == 0)
        pb.Image = Properties.Resources.X;
    else
        pb.Image = Properties.Resources.O;

    NumberChoise++;
}
```

**Concepts practiced:** event handling, `sender` casting, `Tag` property, class-level fields, resources, conditional logic.

## 📁 Project Structure

```
XO-Game-Final/
├── XO-Game-Final.sln        # Solution file
├── Form1.cs                 # Game logic
├── Form1.Designer.cs        # UI layout (auto-generated)
├── Form1.resx               # Form resources
├── Program.cs               # Entry point
├── Properties/
│   └── Resources.resx       # X and O images
└── README.md
```

## 🤝 Contributing

Suggestions and improvements are welcome. Fork the repo, create a branch, and open a pull request.

## 👤 Author

**Abdelhalim**
Self-taught developer learning C# and .NET.

- GitHub: [@YOUR-USERNAME](https://github.com/YOUR-USERNAME)

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

<div align="center">

⭐ If you like this project, give it a star!

</div>
