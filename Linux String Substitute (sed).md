in app server 3 of stratos change few thing in file /Home/BSD.txt

```bash
#delete some word and save the result in diff file named BSD_DELETE 
sed '/\<software\>/d' BSD.txt > BSD_DELETE.txt
cat BSD_DELETE.txt | grep software
cat BSD_DELETE.txt
#replace some word and save the result in a diff file named BSD_REPLACE 
sed 's/\bfrom\b/them/g' BSD.txt > BSD_REPLACE.txt
cat BSD_REPLACE.txt | grep from
cat BSD_REPLACE.txt | grep them
cat BSD_REPLACE.txt 
