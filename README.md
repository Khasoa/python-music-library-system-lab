# Music Library System Lab
## Learning Goals

- Build Python classes to encapsulate real-world entities.

- Use instance attributes for individual object data.

- Use class attributes to track global insights across all objects.

- Implement class methods to manipulate class-level data.

- Apply OOP principles for scalable data tracking and analytics.

## Introduction

In this lab, you will create a Music Library System to manage and analyze a collection of songs. Each song will have attributes like name, artist, and genre. The system also keeps track of global statistics: the total number of songs, all unique artists and genres, and counts of songs per artist and genre. This functionality simulates features found in music streaming services, including analytics and recommendation engines.

## Setup Instructions
- Fork and Clone the Repository

- Go to the provided GitHub repository link.

- Fork the repository to your GitHub account.

- Clone the forked repository to your local machine:

. git clone <repo-url>
. cd course-7-module-2-python-music-library-system-lab

. Install Dependencies

. Ensure Python is installed:

. python --version

- Run tests with pytest:

pytest

### Task 1: Define the Song Class
- Instance Attributes

Each Song object should store:

name – the name of the song

artist – the artist of the song

genre – the genre of the song

- Class Attributes

The Song class also keeps track of:

count – total number of songs created

genres – list of unique genres

artists – list of unique artists

genre_count – dictionary counting songs per genre

artist_count – dictionary counting songs per artist

- Class Methods

Each method is triggered when a new song is created:

add_song_to_count() – increments count by 1

add_to_genres() – adds the genre to genres if not already present

add_to_artists() – adds the artist to artists if not already present

add_to_genre_count() – increments genre count or initializes it to 1

add_to_artist_count() – increments artist count or initializes it to 1

### Task 2: Implement Initialization

In song.py:

class Song:
    count = 0
    genres = []
    artists = []
    genre_count = {}
    artist_count = {}

    def __init__(self, name, artist, genre):
        self.name = name
        self.artist = artist
        self.genre = genre

        Song.count += 1
        Song.add_to_genres(genre)
        Song.add_to_artists(artist)
        Song.add_to_genre_count(genre)
        Song.add_to_artist_count(artist)

### Task 3: Push Feature Branch & Open PR

Create a feature branch:

git checkout -b song-class


Commit changes:

git add song.py
git commit -m "Add Song class with analytics"


Push branch to GitHub:

git push origin song-class


Open a Pull Request from song-class to main.

Merge after review.

### Task 4: Best Practices

Use clear docstrings and comments.

Ensure class attributes are updated via class methods.

Maintain consistent naming for class attributes (artist_count, genre_count).

Keep tests passing using pytest before merging.

## Conclusion

By completing this lab, you will:

1. Master class and instance attributes in Python.

2. Track and aggregate data across objects with class attributes.

3. Build scalable analytics for a music library.

4. Apply OOP techniques that reflect real-world software engineering practices.