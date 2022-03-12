# My Meme!

![my_meme](https://user-images.githubusercontent.com/101376063/157794719-bd6e49ab-0b4c-4613-895e-ec2256844fa6.png)

## Meme Insparation 
This meme is inspred by one of my close friends. Using Winnie the Pooh to caputure the two stages he goes through after a long night out is not only very accurate, but hilarious too! Not to metion the use of the all time Font MVP **"Comic Sans"** which is a decision that goes without saying!

## Meme Code
` library(magick) `

` one <- image_read("https://th.bing.com/th/id/R.45540a78ccb543a0689778f0ba880ec5?rik=L2y4GrZKZrz%2fuQ&pid=ImgRaw&r=0") %>%
  image_scale(500) `

` two <- image_read("https://i.redd.it/soiawastzla41.jpg") %>%
  image_scale(500) `

 ` first <- image_blank(width = 500, height = 500, color = "#000000") %>%
  image_annotate(text = "Night\nBefore", color = "#ffffff", size = 80, font = "comic sans", gravity = "center") `

` second <- image_blank(width = 500, height = 500, color = "#000000") %>%
  image_annotate(text = "Night\nAfter", color = "#ffffff", size = 80, font = "comic sans", gravity = "center") `

` first_rows <- c(one, first) %>%
  image_append() `
  
` second_row <- c(two, second) %>%
  image_append() `

` my_meme <- c(first_rows, second_row) %>%
  image_append(stack = TRUE) `

` image_write(my_meme, "my_meme.png") `
