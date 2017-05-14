---
layout: post
title: "Blueflag/BigDatr Music Analysis"
date: 2014-05-30
---

Music tastes can be super varied from one person to the next. I don't know why I like a lot of the music I do (a good subject for a future analysis).
The music we listen to in the space of a day can also be be super varied....or not. This is an analysis into the music habits of Blueflag/BigDatr employees.

The main questions this analysis is seeking to answer is:
- What are the most popular songs we have played?
- Who are the most popular artists?
- What are the most popular albums?
- What genres do we listen to the most? What country of origin do we listen to the most? What time period is most popular?
- What is the mood of the songs being played? What is the most dominant mood? What is a playlist of songs to fit a mood?
- Does the weather have an impact on what music we play?

#### Data Sources:
 - LastFM API - blueflagmusic account
 - MusicBrainz API - Song, Album, Artist metadata

---

## Artists
The first thing I looked at was the number of times we have played a song, grouped by artist. Surprisingly (to me atleast), `The National` came out on top followed by `Queen` and `TV on the Radio`.
I don't feel like we actually listen to these artists aaaaall the time, so the next part of the artist analysis will be to look at the most common artists we play by day, rather than just relying on
the track count (E.g We have heard Queen on 20% of the days where music has been played). Or even the probability you will hear an artist on any given day.

![rplot](https://cloud.githubusercontent.com/assets/18128531/26030907/0d891434-38a5-11e7-9738-3e992a325791.png)

---

## Albums
The next area I looked at was Albums. `The Platinum Collection - Queen` came out on top as the most played album. Great album, at 340 plays we still don't play it enough! `Feel Good - Gorillaz` came in at number two, with `Random Access Memories - Daft Punk` rounding out the top three. Not too bad.

![queen](https://cloud.githubusercontent.com/assets/18128531/26032884/08dd5e76-38e2-11e7-9e1a-d893501f76f0.gif)
![daftunk](https://cloud.githubusercontent.com/assets/18128531/26032891/2d3204ac-38e2-11e7-8155-9ddcdf61e34c.gif)
![gorillaz](https://cloud.githubusercontent.com/assets/18128531/26032894/3b2ee0fc-38e2-11e7-90f4-0ccae411a276.gif)


There are a few other interesting albums that make it into the top 20, indicating that plays alone is really not a great way to understand if we're listening to albums alot or just
queuing a bunch of songs in one go that make it appear as though we listen to them a-lot.

![rplot](https://cloud.githubusercontent.com/assets/18128531/26032584/3953ddb2-38da-11e7-9921-ae600f8680d1.png)

---

### Songs
Next up - songs. `Uptown Funk - Mark Ronson` takes spot number one. `Riptide - Vance Joy` at number two. Ugh. And `Lean On - Major Lazer` taking out number three.

It would be interesting to see if we tend to play more individual songs or albums - another reason to get some data around the time that we play the songs instead of just pre-aggregated data.

![rplot](https://cloud.githubusercontent.com/assets/18128531/26032980/0c2f776a-38e4-11e7-83d7-861816f04668.png)

---

### Next Steps
This is a pretty basic analysis, from here I will look at:

- Join with the data from MusicBrainz which includes - Genre, Tags, Country of origin, years active and more
- Try and find some data on the moods associated with these songs. Are we a happy/sad/energetic office
- Get the lyrics for each song (Then look at a [Markov Chain](http://setosa.io/ev/markov-chains/) of songs to create our own song from the songs we like)
- Look into getting data from LastFM that includes more data around the specific times we play each song
- Categorise and cluster songs to see what our dominant listening tendencies are
- See how we compare with others who have rated songs/albums/artists
