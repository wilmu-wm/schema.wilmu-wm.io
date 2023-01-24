# WilmU SEO Documentation Website


## SEO
  ## Table of contents
1. [Schema](#schema)
2. [Structured data that Google supports](#supported)
    1. [Articles](#articles)
    2. [Breadcrumb](#breadcrumb)
    3. [Carousel](#carousel)
    4. [Course](#course)
       1. [Required and Recommended Parameters](#parameters)
    5. [Estimated Salary](#salary)
    6. [Event](#event)
    7. [FAQ](#faq)
    8. [How-To](#howto)
    9.  [Learning Video](#learningvideo)
    10. [Local Business](#localbusiness)
    11. [Logo](#logo)
    12. [Q&A](#qa)
    13. [Sitelinks Search box](#searchbox)
    14. [Speakable](#speakable)
    15. [Video](#video)
3. [Another paragraph](#paragraph2)


### <a name="schema"></a>Schema
Schema documentation for Wilmington University's SEO projects. The wiki contains examples and related schema's associated with wilmu.edu web content.



- 
### <a name="supported"></a>Structured data that Google supports 
**This is a partial list that contains only data that benefits Wilmington University.**


#### <a name="articles">Articles</a>
[Reference](https://developers.google.com/search/docs/appearance/structured-data/article)

#### <a name="breadcrumbs">Breadcrumbs</a>
[Reference](https://developers.google.com/search/docs/appearance/structured-data/breadcrumb)

#### <a name="carousel">Carousel</a>
[Reference](https://developers.google.com/search/docs/appearance/structured-data/carousel)**
Rich results that display in a sequential list or gallery from a single site. This feature must be combined with one of the following features: Course. (e.g., multiple courses)


#### <a name="course">Course</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/course)**
Educational courses that appear in a provider-specific list. Courses can include the course title, provider, and a short description.

**<a name="parameters"></a>Required and Recommended Parameters**

Bold: **Required** Normal: Highly Recommended

| Parameter         | Example Value                                                                                                                                 |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| @type             | Course                                                                                                                                        |
| url               | Find course on [Smart Catalog](https://smartcatalog.co/en/Catalogs/Wilmington-University/Current/)                                            |
| **name**          | English Composition I                                                                                                                         |
| **description**   | This course will help students become more proficient and effective writers, while also developing reading comprehension and analysis skills. |
| provider          | "@type": "Organization",<br>"name": "Wilmington University",<br>"sameAs": "https://www.wilmu.edu"                                             |
| hasCourseInstance | "@type": "CourseInstance",<br>                                                                                                                |
    "courseMode": [<br> 
      "part-time",<br>
      "full-time",<br>
      "distance learning",<br>
      "MOOC",<br>
      "online"   |
| endDate | 2022-03-21 |
| startDate | 2023-02-15 |



```json
<script type="application/ld+json">  

{  
  "@context": "https://schema.org",
  "@type": "Course", 
  "url": "http://smartcatalog.co/en/Catalogs/Wilmington-University/Current/Undergraduate-Catalog/Courses/ENG-English/100/ENG-121",  

  "name": "English Composition I",
  "description": "This course will help students become more proficient and effective writers, while also developing reading comprehension and analysis skills.", 
  "provider": { 
    "@type": "Organization", 
    "name": "Wilmington University",
    "sameAs": "https://www.wilmu.edu"
  },
  "hasCourseInstance": { 
    "@type": "CourseInstance",
    "courseMode": [
      "part-time",
      "full-time", 
      "distance learning",
      "MOOC", 
      "online" 

    ],  
    "endDate": "2022-03-21",  
    "startDate": "2023-02-15"  
  }  
}  
</script> ```

#### <a name="salary">Estimated Salary</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/estimated-salary)**
Salary estimate information, such as salary ranges and region-based salary averages for job types, displayed in the job search experience on Google.

#### <a name="event">Event</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/event)**
An interactive rich result that shows a list of organized events, such as concerts or art festivals, that people may attend at a particular time and place.

#### <a name="faq">FAQ</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/faqpage)**
A Frequently Asked Question (FAQ) page contains a list of questions and answers pertaining to a particular topic.

#### <a name="howto">How-To</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/how-to)**
A How-to walks users through a set of steps to successfully complete a task, featuring video, images, and text (e.g., video tutorials, register, etc.).

#### <a name="learningvideo">Learning Video</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/learning-video)**
Help students and teachers discover and watch educational videos by adding Learning Video structured data to your educational videos.

#### <a name="localbusiness">Local Business</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/local-business)**
Business details displayed in the Google knowledge panel, including open hours, ratings, directions, and actions to book appointments or order items.

#### <a name="logo">Logo</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/logo)**
Your organization's logo in search results and Google knowledge panel.

#### <a name="qa">Q&A</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/qapage)**
Q&A Pages are web pages that contain data in a question and answer format, which is one question followed by its answers.

#### <a name="searchbox">Sitelinks Search box</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/sitelinks-searchbox)**
A search box that is scoped to your website when it appears as a search result.

#### <a name="speakable">Speakable</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/speakable)**
==TTS, read news stories??==

#### <a name="video">Video</a>
[Resource](https://developers.google.com/search/docs/appearance/structured-data/video)**
Video information in search results, with the option to play the video, specify video segments, and live-stream content.

## How to generate structured data

There are different ways to generate structured data with JavaScript, but the most common are:

- [Google Tag Manager](https://developers.google.com/search/docs/appearance/structured-data/generate-structured-data-with-javascript#use-google-tag-manager)[^bignote]
- ~~[Custom JavaScript](https://developers.google.com/search/docs/appearance/structured-data/generate-structured-data-with-javascript#custom-javascript)~~
- [Merkle Schema Markup Generator](https://technicalseo.com/tools/schema-markup-generator/)
- [editor.md](https://pandao.github.io/editor.md/en.html)
- [Dillinger](https://dillinger.io/)
- MS Visual Code
  [^bignote]: Here's one with multiple paragraphs and code.

    Indent paragraphs to include them in the footnote.

    `{ my code }`

    Add as many paragraphs as you like.
## Use Google Tag Manager to generate JSON-LD dynamically

To generate structured data with Google Tag Manager, follow these steps:

1.  [Sign in to Google Tag Manager](https://tagmanager.google.com/)
2.  Add a new **Custom HTML** tag to the container.
3.  Paste the desired structured data block into the tag content.
4.  Install the container as shown in the **Install Google Tag Manager** section of your container's admin menu.
5.  To add the tag to your website, publish your container in the Google Tag Manager interface.
6.  [Test your implementation](https://developers.google.com/search/docs/appearance/structured-data/generate-structured-data-with-javascript#testing).

### Using variables in Google Tag Manager

Google Tag Manager (GTM) supports [variables](https://support.google.com/tagmanager/topic/7683268?ref_topic=3441647) to use information on the page as part of your structured data. 
Use variables to extract the structured data from the page instead of duplicating the information in GTM. 

| Built-in variables                                                                                     | User-defined variables                                                                                                      |
| ------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------- |
| For [web containers](https://support.google.com/tagmanager/answer/7182738?hl=en&ref_topic=7182737)     | For [web](https://support.google.com/tagmanager/answer/7683362?hl=en&ref_topic=9125128)                                     |
| For [web containers](https://support.google.com/tagmanager/answer/7182738?hl=en&ref_topic=7182737)     | For [mobile](https://support.google.com/tagmanager/answer/7683157?hl=en&ref_topic=9125128)                                  |
| For [iOS containers](https://support.google.com/tagmanager/answer/7182836?hl=en&ref_topic=7182737)     | [Format values in user-defined web variables](https://support.google.com/tagmanager/answer/9121006?hl=en&ref_topic=9125128) |
| For [Android containers](https://support.google.com/tagmanager/answer/7182414?hl=en&ref_topic=7182737) |                                                                                                                             |
#### Built-in variables
-  For [web containers](https://support.google.com/tagmanager/answer/7182738?hl=en&ref_topic=7182737).
- For [web containers](https://support.google.com/tagmanager/answer/7182738?hl=en&ref_topic=7182737).
- For [iOS containers](https://support.google.com/tagmanager/answer/7182836?hl=en&ref_topic=7182737).
- For [Android containers](https://support.google.com/tagmanager/answer/7182414?hl=en&ref_topic=7182737).

#### Create custom user-defined variables in Google Tag Manager
Create custom user-defined variables in Google Tag Manager to suit specific requirements that might not already be covered by [built-in variables](https://support.google.com/tagmanager/topic/7182737).
To create a new user-defined variable:
1.  In the left navigation, click **Variables**.
2.  In the User-Defined Variables section, click **New**.
3.  Click **Variable Configuration** and select the desired variable type. 
4.  Complete the options for the selected variable type.
5.  Name the variable. Use a naming scheme that is descriptive of the variable's function, e.g. "_Data Layer Variable - Product Name_."
6.  Click **Save**.

For example, you can dynamically create a [Recipe](https://developers.google.com/search/docs/appearance/structured-data/recipe) JSON-LD block that uses the page title as the recipe name by creating the following custom variable named `recipe_name`:

```javascript
function()  {  return document.title;  }
```

You can then use `{{recipe_name}}` in your custom tag HTML.

We recommend to create variables to collect all the necessary information from the page using variables.

Here is an example for the custom HTML tag content:
Assumes that you defined the variables recipe_name, recipe_image and recipe_author in GTM.
```json
<script type="application/ld+json">  
  {  
    "@context":  "https://schema.org/",  
    "@type":  "Recipe",  
    "name":  "{{recipe_name}}",  
    "image":  [ "{{recipe_image}}" ],  
    "author":  {  
    "@type":  "Person",  
    "name":  "{{recipe_author}}"  
  }  
}  
</script>```