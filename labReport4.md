## Links: 
[Link to my markdown-parse repository](https://github.com/ZhouYuantian/markdown-parser)

[Link to the one I reviewed in week 7](https://github.com/katieki/markdown-parser)

## For Snippet1:
Expected Output:
```
[url.com, `google.com, google.com, ucsd.edu]
```
Code in MarkdownParseTest.java:
```
@Test
    public void getLinksTest_snip1() throws IOException {
        Path fileName = Path.of("test-Snippet1.md");
        String content = Files.readString(fileName);
        List<String> result = List.of("url.com","`google.com","google.com","ucsd.edu");
        assertEquals(result, MarkdownParse.getLinks(content));
    }
```
For My implementation: The test passed

![image](https://user-images.githubusercontent.com/46364362/169369965-4131e243-19a9-49f3-9209-f52a386a6111.png)


For the Implementation I Reviewed in Week 7: The test failed

![image](https://user-images.githubusercontent.com/46364362/169363067-d841a5a8-8cfd-49aa-98f8-ff244cb8d903.png)

## For Snippet2:
Expected Output:
```
[a.com, a.com(()), example.com]
```
Code in MarkdownParseTest.java:
```
@Test
    public void getLinksTest_snip2() throws IOException {
        Path fileName = Path.of("test-Snippet2.md");
        String content = Files.readString(fileName);
        List<String> result = List.of("a.com","a.com(())","example.com");
        assertEquals(result, MarkdownParse.getLinks(content));
    }
```
For My implementation: The test failed
![image](https://user-images.githubusercontent.com/46364362/169370550-99e1b8f5-30d1-43b5-8025-3232b6aa7032.png)




For the Implementation I Reviewed in Week 7: The test failed

![image](https://user-images.githubusercontent.com/46364362/169363924-d4a808fa-fd92-408c-b307-5a2237274f42.png)


## For Snippet3:
Expected Output:
```
[https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, https://cse.ucsd.edu/]
```
Code in MarkdownParseTest.java:
```
@Test
    public void getLinksTest_snip3() throws IOException {
        Path fileName = Path.of("test-Snippet3.md");
        String content = Files.readString(fileName);
        List<String> result = List.of("https://www.twitter.com","https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule","https://cse.ucsd.edu/");
        assertEquals(result, MarkdownParse.getLinks(content));
    }
```
For My implementation: The test failed
![image](https://user-images.githubusercontent.com/46364362/169370766-2625c0d4-e6e9-432b-9059-d78ba4933247.png)

![image](https://user-images.githubusercontent.com/46364362/169370876-fd1751eb-72f7-43a7-aade-8b843d075297.png)

For the Implementation I Reviewed in Week 7: The test failed
![image](https://user-images.githubusercontent.com/46364362/169364634-b6671226-68b0-457f-ba9f-021aaa793b73.png)

![image](https://user-images.githubusercontent.com/46364362/169364551-d2adcb56-6718-42a7-a66e-3d8723261209.png)

## Answer the questions:

1. My program passed the Snippet1 test case.
2. For snippet2, I think is possible to make it work by a samll edit, we just need to add a if statement to check whether the close parentheses is the last on or not. We just need to consider the first open parentheses and the last close parentheses, and treat all others between them as part of the link.
3. For snippet3, I don't think we can fix it within 10 line code, since we need two if statement to check both parentheses and brackets for deciding whether it is the true symbol of the link or it is some text needed to be ignore. And also, we need to edit the code to make it ignore the line breaks.

