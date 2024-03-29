<template>
    <section id="about">
        <article>
            <h2>Overview</h2>
            <p>
                I’m a very hard-working, motivated and personable data professional, who recently graduated from one of Australia’s highest-ranking universities, The University of Queensland, with a bachelor's degree in Computer Science. While completing this degree I fell in love with the theory and concepts of relational databases, artificial intelligence, and machine learning and as a result, chose Data Science as the major for my degree. While studying I also chose to work casually at the university by helping to teach and develop content for a first-year <a href="https://my.uq.edu.au/programs-courses/course.html?course_code=INFS1200" target="_blank" rel="noopener noreferrer">course</a> on relational databases and SQL. During my time at university, I was able to learn about and use many different data-driven concepts and tools including:
                
                <BulletPoints :points="dataScienceConcepts" id="dataScienceConcepts"/>

                I also spent a large portion of time during my degree learning about concepts for software development and computer science such as:

                <BulletPoints :points="computerScienceConcepts" id="computerScienceConcepts"/>

                Coming into my final year of study I also completed a twelve-week internship at the Bank Of Queensland, where I was able to put much of the theory taught in my degree to practical use; working on several projects and utilizing several industry standard tools including: Azure Data Factory, Microsoft Power BI, Microsoft SQL Server and Azure Blob Storage.<br/><br/>

                <!-- <BulletPoints :points="internshipTechnologies" id="internshipTechnologies"/> -->

                Immediately after graduating, I returned to BOQ and began my current role as an Associate Data Operations Engineer, where I work 50% on projects and 50% of data operations support and maintenance. In this role I have gained proficiency in using:

                <BulletPoints :points="graduateJobTechnologies" id="graduateJobTechnologies"/>
            </p>
            <h2>Programming Languages</h2>
            <p>
                Below is a list of programming languages I have experience using. Each language also has a rating of how comfortable I am using the language.

                <ProgrammingLanguage :languages="languageList"/>
            </p>
            <h2>Technologies</h2>
            <p>
                Below are some of the main programming technologies I've used and am familiar with.
            </p>
            <Gallery :imgs="techPics"/>
        </article>
    </section>
</template>

<script>
import BulletPoints from "@/components/BulletPoints.vue"
import ProgrammingLanguage from "@/components/ProgrammingLanguage.vue"
import Gallery from "@/components/Gallery.vue"

export default {
    name: "AboutView",
    components: {
        BulletPoints,
        ProgrammingLanguage,
        Gallery
    },
    methods: {
        getImgUrl(pic) {
            return require('../assets/img/technologies/'+pic)
        }
    },
    data() {
        return {
            test: "ADF.png",
            dataScienceConcepts: [
                'Artificial Intelligence',
                'Machine Learning and Data Mining',
                'Relational and Non-relational Databases',
                'Distributed Database Systems',
                'Data Warehousing',
                'Cloud Computing',
                'Working with High Dimensional Spatial and Multimedia Data',
                'Architecture for Big Data'
            ],
            computerScienceConcepts: [
                'Object Oriented Programming',
                'Functional Programming and Lambda Calculus',
                'Advanced Algorithms and Data Structures',
                'Low-level C, Assembly and Computer Architecture',
                'Quantum Computing',
                'Program Design and Version Control'
            ],
            internshipTechnologies: [
                'Azure Data Factory',
                'Microsoft Power BI',
                'Microsoft SQL Server',
                'Azure Blob Storage'
            ],
            graduateJobTechnologies: [
                'Azure Data Factory',
                'Azure Databricks',
                'Azure DevOps',
                'Jira',
                'Confluence'
            ],
            languageList: [
                {name: "Python", rating: "five"},
                {name: "Java", rating: "four"},
                {name: "Dart", rating: "three"},
                {name: "C", rating: "four"},
                {name: "SQL", rating: "five"},
                {name: "MATLAB", rating: "three"},
                {name: "R", rating: "one"},
                {name: "Scala", rating: "one"},
                {name: "JavaScript", rating: "two"},
                {name: "PHP", rating: "three"},
                {name: "HTML", rating: "five"},
                {name: "CSS", rating: "four"},
                {name: "Shell", rating: "four"}
            ],
            techPics: [
                {name: "ADF.png", alt: "Azure Data Factory"},
                {name: "azure.png", alt: "Microsoft Azure"},
                {name: "bootstrap.png", alt: "Bootstrap"},
                {name: "confluence.png", alt: "Confluence"},
                {name: "databricks.png", alt: "Databricks"},
                {name: "devops.png", alt: "Azure Devops"},
                {name: "flutter.png", alt: "Flutter"},
                {name: "gcp.png", alt: "Google Cloud Platform"},
                {name: "github.png", alt: "GitHub"},
                {name: "hadoop.png", alt: "Hadoop"},
                {name: "intellij.png", alt: "IntelliJ"},
                {name: "jira.png", alt: "Jira"},
                {name: "jQuery.png", alt: "jQuery"},
                {name: "linux.png", alt: "Linux"},
                {name: "matplotlib.png", alt: "Matplotlib"},
                {name: "mySQL.png", alt: "MySQL"},
                {name: "numpy.png", alt: "NumPy"},
                {name: "oracle.png", alt: "Oracle"},
                {name: "pandas.png", alt: "Pandas"},
                {name: "powerBI.png", alt: "Microsoft PowerBI"},
                {name: "pytorch.png", alt: "PyTorch"},
                {name: "scikitLearn.png", alt: "ScikitLearn"},
                {name: "spark.png", alt: "Apache Spark"},
                {name: "SQLite.png", alt: "SQLite"},
                {name: "sqlServer.png", alt: "Microsoft SqlServer"},
                {name: "vscode.png", alt: "Visual Studio Code"},
                {name: "vue.png", alt: "Vue"},
                {name: "jupyter.png", alt: "Jupyter Notebooks"}
            ]
        }
    }
}
</script>

<style>
section {
    margin-top: 150px
}

article {
    max-width: 1500px;
    margin: auto;
}

article h2 {
    margin-left: 100px;
    margin-top: 30px;
}

article p {
    margin: 30px 100px 0px 100px;
    font-size: 1.7em;
}

article a {
    color: var(--accent-bright);
    text-decoration: none;
    font-size: 1em;
}

article a:hover {
    text-decoration: underline;
}

/* Tablet size */
@media screen and (max-width: 740px) {
    section {
        margin-top: 50px;
    }
}
</style>