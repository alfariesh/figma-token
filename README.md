
# Design Token Systems

Sistem design token yang fleksibel dan dapat disesuaikan untuk mendukung multiple brand dan tema dengan aksesibilitas AAA compliance.

## 🎨 Struktur Token

### Seed Tokens
**Lokasi:** `/seed/`
- **colors.json** - Palet warna dasar dengan variasi tonal lengkap
- **dimensions.json** - Sistem ukuran dan spacing
- **typography.json** - Font families dan typographic scales

### Core Tokens
**Lokasi:** `/core/`
- **dimensions.json** - Core dimensional system
- **override/brands/** - Brand-specific color mappings
- **override/contrast/** - High contrast variants untuk aksesibilitas
- **override/mode/** - Light/dark mode configurations

### Semantic Tokens
**Lokasi:** `/semantic/`
- **color.json** - Role-based color tokens (action, feedback, neutral, etc.)
- **dimension.json** - Semantic spacing system
- **text.json** - Typography roles dan hierarchy

### Output Tokens
**Lokasi:** `/output/`
- **component.json** - Component-specific tokens
- **dataViz.json** - Data visualization colors
- **graphic.json** - Graphic design tokens

## 🌈 Brand Variants

### Tersedia 4 Brand Utama:

1. **Blueberries** - Menggunakan palet biru dengan netral mangosteen
2. **Lime** - Menggunakan palet hijau dengan netral morras
3. **Mint** - Menggunakan palet mint dengan netral cyan
4. **Morras** - Menggunakan palet passion dengan netral cranberries

Setiap brand memiliki:
- Light/dark mode variants
- High contrast versions untuk aksesibilitas
- Consistent semantic mappings

## 🎯 Fitur Utama

### Aksesibilitas
- **AAA Compliance** - Rasio kontras 7:1 untuk semua kombinasi teks
- **High Contrast Mode** - Mode khusus untuk pengguna dengan kebutuhan kontras tinggi
- **Consistent Semantics** - Penamaan yang konsisten untuk screen readers

### Sistem Warna
- **Seed-based** - Semua warna berasal dari seed colors yang terdefinisi
- **Tonal Scales** - Setiap warna memiliki 22+ variasi tonal
- **Context-aware** - Warna yang berbeda untuk light/dark mode

### Data Visualization
- **Categorical Colors** - 8 warna berbeda untuk series data
- **Sequential Scales** - Gradasi warna untuk data berurutan
- **Diverging Scales** - Warna untuk data positif/negatif

## 📁 Struktur File

```
├── seed/                   # Token dasar
│   ├── colors.json        # Palet warna seed
│   ├── dimensions.json    # Ukuran dasar
│   └── typography.json    # Font families
├── core/                  # Token inti
│   ├── dimensions.json    # Sistem dimensi
│   └── override/          # Override untuk brand/mode
│       ├── brands/        # Brand-specific mappings
│       ├── contrast/      # High contrast variants
│       └── mode/          # Light/dark mode
├── semantic/              # Token semantik
│   ├── color.json        # Role-based colors
│   ├── dimension.json    # Semantic spacing
│   └── text.json         # Typography roles
├── output/               # Token output
│   ├── component.json    # Component tokens
│   ├── dataViz.json      # Data viz colors
│   └── graphic.json      # Graphic tokens
├── $themes.json          # Tema configurations
└── $metadata.json        # Metadata sistem
```

## 🚀 Penggunaan

### Referensi Token
```json
{
  "background": {
    "value": "{base.color.neutral.background.default}",
    "type": "color"
  }
}
```

### Brand Selection
Pilih brand dengan mengaktifkan token set yang sesuai:
- `core/override/brands/Blueberries`
- `core/override/brands/Lime`
- `core/override/brands/Mint`
- `core/override/brands/Morras`

### High Contrast Mode
Aktifkan `core/override/contrast/highContrast` untuk mode kontras tinggi.

## 🎨 Color Palette

### Seed Colors
- **Blueberries** - #f6f7fd hingga #00010A (22 variasi)
- **Lime** - #f9fdf7 hingga #040802 (22 variasi)
- **Mint** - #F3FCFC hingga #011314 (22 variasi)
- **Passion** - #FAF5F6 hingga #090104 (22 variasi)

### Accent Colors
- **Carrot** - Orange palette untuk warnings
- **Chilli** - Red palette untuk errors
- **Cucumber** - Green palette untuk success
- **Sky** - Blue palette untuk informational

## 🛠️ Development

### Figma Integration
Token system terintegrasi dengan Figma Variables:
- Auto-sync dengan Figma Variables
- Style references untuk colors dan typography
- Collection management untuk multi-brand

### Version Control
Gunakan Git tags untuk version management:
```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
git push origin v1.0.0
```

## 📊 Data Visualization

### Categorical Series
8 warna berbeda untuk data series dengan state:
- Default
- Hover
- Muted/inactive

### Chart Components
- Grid lines dan axis styling
- Tooltip styling
- Legend components
- Selection dan annotation colors

## 🔧 Customization

### Menambah Brand Baru
1. Buat file baru di `core/override/brands/`
2. Map seed colors ke brand tokens
3. Tambahkan high contrast variants
4. Test aksesibilitas

### Mengubah Spacing
Edit `core/dimensions.json` untuk mengubah spacing system dasar.

## 📝 Contributing

1. Fork repository
2. Buat branch feature (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push ke branch (`git push origin feature/amazing-feature`)
5. Buat Pull Request

## 📄 License

Design Token System ini menggunakan lisensi MIT. Lihat file `LICENSE` untuk detail lebih lanjut.

---

**Catatan:** Sistem ini dirancang untuk mendukung aksesibilitas AAA dan multi-brand consistency. Pastikan untuk menguji kontras warna sebelum implementasi.
