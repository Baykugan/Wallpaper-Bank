# Wallpaper Bank

A small wallpaper collection organized by category.

## Clone everything

```bash
git clone https://github.com/Baykugan/Wallpaper-Bank.git
cd Wallpaper-Bank
git lfs pull
```

## Clone selected categories

### Option 1: Sparse checkout

Use this when you only want selected folders in your working directory.

```bash
git clone --filter=blob:none --sparse https://github.com/Baykugan/Wallpaper-Bank.git
cd Wallpaper-Bank
git sparse-checkout set wallpaper-bank/anime wallpaper-bank/illustrations
git lfs pull
```

Replace `wallpaper-bank/anime` and `wallpaper-bank/illustrations` with the categories you want.

### Option 2: LFS include/exclude only

Use this when you want the full folder structure, but only want to download selected LFS files.

```bash
git clone https://github.com/Baykugan/Wallpaper-Bank.git
cd Wallpaper-Bank
git lfs pull --include="wallpaper-bank/anime/**,wallpaper-bank/illustrations/**"
```

Replace the paths inside `--include` with the categories you want.
