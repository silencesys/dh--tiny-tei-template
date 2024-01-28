# Tiny template for TEI editions

Have you ever run a workshop on TEI and then struggled with where or how to publish the students' work? This template was created for that very reason. It has been designed to be as simple as possible, while still allowing students to make at least some adjustments so that they feel a sense of ownership over their work.

## Limitations
- It does not work with images
- It does not work with multiple files
- It does not work very well with different readings

However in future versions I hope to address these issues and extend the functionality of the template. If you have any suggestions, please let me know.

## How to use this template
1. You can either fork this repository or download it as a zip file in the release section.
2. Copy your XML edition to the `xml` folder.
3. Edit the `index.html` file to include the correct path to your XML file. Look for following line
  ```html
  <script>
    var CETEIcean = new CETEI()
    CETEIcean.getHTML5("xml/[name_of_your_file].xml", function(data) {
      document.getElementById("TEI").appendChild(data)
    })
  </script>
  ```
4. You can tweak colour, text-size etc. in the `config.css` file at the root of the repository.
5. Publish it on GitHub pages or any other web-server.

## Publishing on GitHub pages
1. Create a new repository on GitHub.
2. Upload the files from the template to the repository.
3. Go to the settings of the repository and scroll down to the GitHub pages section.
4. Select the `master` branch as the source and click save.
5. Wait a few minutes and then click on the link provided in the GitHub pages section.

## Copyright and licence
This template is released under the [MIT licence](LICENSE.md) and is free to use, modify and redistribute. The example XML file should be considered as a demonstration of the template and is not covered by the licence.

This template uses the [CETEIcean](https://github.com/TEIC/CETEIcean) library, which is released under the [BSD 2-Clause "Simplified" License](https://github.com/TEIC/CETEIcean/blob/master/LICENSE.md).
