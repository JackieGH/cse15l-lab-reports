## Servers and Bugs ##
### Part 1 ###
### Part 2 ###
Testing Methods in ArrayExamples.java <br>
A failure-inducing input for **reverseInPlace Method**: <br>
`
@Test
  public void testReverseInPlace1() {
    int[] input2 = {1,2,3};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{3,2,1}, input2);
  }

`
### Part 3 ###
In Week 2, deciphering the parts of a URL was an insightful discovery that made building a server less daunting. I had tested HTML, CSS, and JavaScript code on a temporary server before for another class -- COGS 3. However, the way I launched a temporary server was through VSCODE's `Publish` option, so I never really knew how this happened without the editor. I also bought a domain about a year ago, but never made anything on it. So it's more of a parked domain. Now, I feel hopeful about actually being able to develop some content because I'm more knowledgeable about how webpages are working. I'm especially interested in how I can generate simple interactive changes that a user can see just from the updates we made to our server in Lab 2.
