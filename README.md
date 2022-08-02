# Git-bash

<h1 align="center">Task 1:</h1>


1) See where I am -- ``` pwd ```

2) Create folder -- ``` mkdir folder ```

3) Go to the folder -- ``` cd folder/ ```

4) Create 3 folders -- ``` mkdir qa1 qa2 qa3 ```

5) Go to any folder -- ``` cd qa1/ ```

6) Create 5 files (3 txt, 2 json) -- ``` touch file1.txt file2.txt file3.txt file4.json file5.json ```

7) Create 3 folders -- ``` mkdir b1 b2 b3 ```

8) List folder contents -- ``` ls ```

9)   
   + Open any txt file -- ``` cat >> file1.txt ```

   + write something there, any text -- ``` (text){press ENTER} ```
   
   + save and exit -- ``` {press CTRL+C} ```
   
10) Exit the folder one level up -- ``` cd ../ ```

11) move any 2 files you created to any other folder -- ``` mv qa1/{file4.json,file5.json} qa2 ```

12) copy any 2 files you created to any other folder -- ``` cp qa1/{file2.txt,file3.txt} qa2 ```

13) Find file by name -- ``` find -name file3.txt ```

14) view content in real time -- ``` tail -F qa1/file1.txt ```

15) output the first few lines from a text file -- ``` head qa1/file1.txt ```

16) output the last few lines from a text file -- ``` tail qa1/file1.txt ```

17) view the contents of a long file -- ``` less qa1/file1.txt ```

18) display date and time -- ``` date ```


<h3 align="center">Send an http request</h3>

*Exercise

Send an http request to the server.

http://162.55.220.72:5005/terminal-hw-request

``` curl "http://162.55.220.72:5005/get_method?name=Bezirgen&age=22" ```

<h3 align="center">Write a script</h3>

Write a script that will automatically execute steps 3, 4, 5, 6, 7, 8, 13:

1) Create a file + write a script there -- ``` cat >> script.txt ```
 
 ```
#!/bin/bash
mkdir folder
cd folder
mkdir qa1 qa2 qa3
cd qa1
touch file1.txt file2.txt file3.txt file4.json file5.json
mkdir b1 b2 b3
ls
cd..
mv qa1/{file4.json,file5.json} qa2/
```

2) save and exit -- ``` {press CTRL+C} ```
       
3) make file executable -- ``` chmod +x ./script.txt ```
       
4) run script -- ``` ./script.txt ```

<h3 align="center">==============================================</h3>
       
<h1 align="center">Task 2:</h1>       
       
 1. Make folder dir_1 -- ``` mkdir dir_1 ```

 2. Go to the folder dir_1 -- ``` cd dir_1/ ```
 
 3. Create folder inner_dir_1 -- ``` mkdir inner_dir_1 ```
 
 4. See where you are -- ``` pwd ```
 
 5. Being in the dir_1 folder, create an empty text file tf_1.txt -- ``` touch tf_1.txt ```
 
 6. Being in the dir_1 folder, use the ``` cat ``` command to create a text file tf_2.txt with the following lines:


- the first 1
- second 2
- the third 3


``` cat >> tf_2.txt ```


- the first 1
- second 2
- the third 3


``` {press CTRL+C} ```

 7. Go to the folder inner_dir_1 -- ``` cd inner_dir_1/ ```
 
 8. Through ``` cat ```, make a text file tf_3.txt with any lines:
 
``` cat >> tf_3.txt ```

- the fourth 4
- the fifth 5

``` {press CTRL+C} ```       
       
 9. Through cat, add the line “the second 2” to the text file tf_3.txt -- ``` cat >> tf_3.txt ```

 10. Through cat add the line “the sec 2” to the text file tf_3.txt -- ``` cat >> tf_3.txt ```
 
 11. Through cat add the line “the sec 3” to the text file tf_2.txt -- ``` cat >> ../tf_2.txt ```
 
 12. Through cat add the line “the SeCoNd 2” to the text file tf_3.txt -- ``` cat >> tf_3.txt ```
 
 13. Through cat add the line “the seConD 2” to the text file tf_2.txt -- ``` cat >> ../tf_2.txt ```
 
 14. Make a text file tf_4.txt with 15 lines -- ``` seq 14 |xargs -Iz echo ''>> tf_4.txt ```
 
 15. Make a text file tF_5.txt with 13 lines -- ``` seq 12 |xargs -Iz echo ''>> tf_5.txt ```
 
 16. List all files in a folder -- ``` ls -la ```
 
 17. Exit the folder inner_dir_1 -- ``` cd .. ```       
       
 18. Output the contents of the tf_3.txt file to the terminal -- ``` cat inner_dir_1/tf_3.txt ```
 
 19. Find the path to the file tf_4.txt -- ``` find -name tf_4.txt ```
 
 20. Clear the file tf_4.txt from the contents without deleting the file itself -- ``` inner_dir_1/tf_4.txt ```
 
 21. Find the path to files that have "tf" in the name -- ``` find . -name '*tf*.*' ```
 
 22. Find the path to files that have "tf" in the name and letters in any case -- ``` find . -iname '*tf*.*' ```
 
 23. Find lines in files where there is a combination of letters “sec” in the current folder -- ``` grep 'sec' *.* ```
 
 24. Find lines in files where there is a combination of letters “sec” in any case in the current folder -- ``` grep -i 'sec' *.* ```
 
 25. Find lines in files where there is only a combination of letters “sec” in the current folder -- ``` grep -w 'sec' *.* ```
 
 26. Find lines in files where there is only a combination of letters “sec” in any case in the current folder -- ``` grep -iw 'sec' *.* ```   
 
 27. Find lines in files where there is a combination of letters “second” in the current folder --  ```grep 'second' *.* ```
 
 28. Find lines in files where there is a combination of letters “second” in any case in the current folder -- ``` grep -i 'second' *.* ```
 
 29. Find lines in files where there is a combination of letters “second” in all folders below the level -- ``` grep -h 'second' */* ```
 
 30. Find only the path and file name in the lines that contain the combination of the letters “second” in the current folder -- ``` grep -l second *.* | xargs find -name ```
 
 31. Find all lines in all files where there is no “second” combination -- ``` grep -vr 'second' * ```
 
 32. Find only the name and path to files where there is no “second” combination -- ``` grep -Lr second | find ```
 
 33. Output the last 4 lines of any text file to the terminal -- ``` tail -4 tf_2.txt ```
 
 34. Output to terminal 4 the first lines of any text file -- ``` head -4 tf_2.txt ```
 
 35. Command in one line. Create folder and create text file with contents -- ``` mkdir inner_dir_2 | echo 'content' >> tf_9.txt ```
 
 36. Command in one line. Move to any one folder text files that have the word “sec” in their contents -- ``` grep -lw sec */* | xargs mv -t inner_dir_2 ```
 
 37. Command in one line. Copy to any one folder text files that have the word “sec” in their contents -- ``` grep -lw sec */* | xargs cp -t inner_dir_1 ```
 
 38. Command in one line. Find all lines c "sec" in all text files, copy and paste these lines into one new text file created -- ``` grep -h 'sec' */* >> tf_0.txt ```
 
 39. Command in one line. Delete text files that have the word “sec” in their content -- ``` grep -l 'sec' {*.*,*/*} | xargs rm -v ```
 
 40. Just print the line “Good job!!” -- ``` echo 'Good Job!!' ```
 
 
 
 
 
 
