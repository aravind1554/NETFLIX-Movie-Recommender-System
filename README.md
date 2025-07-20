# Movie Recommender System

A comprehensive movie recommendation website built with React, TypeScript, and Tailwind CSS using the TMDB 10K movies dataset.

## Features

- **Smart Recommendations**: Content-based filtering using genre similarity, ratings, release years, cast, and director matching
- **Multiple View Modes**: Popular movies, top-rated movies, and search results
- **Advanced Filtering**: Filter by genre, rating, release year, and language
- **Interactive UI**: Responsive design with movie cards, detailed modals, and smooth animations
- **Search Functionality**: Search by title, genre, cast, or director

## Dataset

This project uses the "Top Rated TMDB Movies 10K" dataset from Kaggle. The dataset should be placed in the `public` folder as `top10K-TMDB-movies.csv`.

## Installation

1. Clone or download this repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Place the dataset file `top10K-TMDB-movies.csv` in the `public` folder
4. Start the development server:
   ```bash
   npm run dev
   ```

## Build for Production

```bash
npm run build
```

## Technologies Used

- React 18
- TypeScript
- Tailwind CSS
- Vite
- Lucide React (for icons)

## Recommendation Algorithm

The system uses content-based filtering with the following factors:
- Genre similarity (highest weight - 40 points)
- Rating similarity (20 points max)
- Release year proximity (20 points max)
- Language matching (5 points)
- Cast/crew overlap (3 points per match)
- Director matching (15 points)

## Project Structure

```
src/
├── components/          # React components
│   ├── MovieCard.tsx   # Individual movie display
│   ├── SearchBar.tsx   # Search and filter interface
│   ├── MovieModal.tsx  # Detailed movie view
│   └── LoadingSpinner.tsx
├── types/              # TypeScript type definitions
│   └── movie.ts
├── utils/              # Utility functions
│   ├── movieData.ts    # Data loading and parsing
│   └── recommendations.ts # Recommendation algorithms
└── App.tsx             # Main application component
```

## License

This project is open source and available under the MIT License.