// Piano Player Test 2

let my_song = [
  { note: 'A', starts_at: 0, lasts: 3 },
  { note: 'F', starts_at: 1, lasts: 3 },
  { note: 'C', starts_at: 1.5, lasts: 1.5 },
  { note: 'B', starts_at: 2.5, lasts: 1 },
  { note: 'A', starts_at: 4, lasts: 5 }
];

let counter = 0;
let songTime = 0;

while (counter < my_song.length){
if (my_song[counter].starts_at == 0){
  console.log("Play " + my_song[counter].note)
  counter++
}
else {
  console.log("Hold for " + (my_song[counter].starts_at - my_song[counter - 1].starts_at));
  console.log("Play " + my_song[counter].note);
  counter++;
}

if (counter == my_song.length){
console.log ("Hold for " + my_song[counter - 1].lasts)
}

  my_song.forEach(function(notes){
    if((notes.starts_at + notes.lasts) == counter){
      console.log("stop playing " + notes.note)
      songTime++;
    } else{
      songTime++;
    }
  });

}

  console.log("Song is finished. Release all notes." );
