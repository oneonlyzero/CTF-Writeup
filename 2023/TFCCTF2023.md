**Event : Fri, 28 July 2023, 18:00 MYT — Sun, 30 July 2023, Organizer : The Few Chosen**

<p align="center">
   <img src="https://github.com/01bst/CTF-Writeup/assets/103404282/daac4fff-3184-4773-8a36-1de04b24b94e" width=300>
</p>

**[Category] Forensic**

1. Download and open the file given within the challenge description `Sus.pcapng` file using `Wireshark`

2. Filter the packet using `http`.

3. You will get the result where there is 3 upload activies, so that mean there is 3 images that has been uploaded.

4. To solve this, first select the packet and view the details by `Follow` the `http`.

5. Change the details view from `ascII` to `Hexdump`(it will make you job a lot easier).

6. In the details you will see a few `information` such as the website visited, the upload page code, and also the image uploaded `hex` value.

7. Copy the image `hex` value and paste it in `Notepad++`.

8. In the `Notepad++`, use `ALT` key and copy the `hex` value only, and paste it in `HxD` tools.

9. Once you pasted it, adjust the `header` with the correct `header` for the image type (PNG).

10. And then save the file as `PNG` eg : solution.png.

11. You will get the result in images.

12. In kali linux, open terminal and use command `zsteg` with `-a` option on the images you get to view the data.

13. Do the same step for each image, and withtin the 3 images, you will get the flag.

Flag : `TFCCTF{H1dd3n_d4t4_1n_p1x3ls_i5n't_f4n_4nd_e4sy_to_f1nd!}`
