<template>
    <NavBar/>
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
        </article>
    </section>
    <ThemeButton/>
</template>

<script>
import NavBar from "@/components/NavBar.vue"
import BulletPoints from "@/components/BulletPoints.vue"
import ThemeButton from "@/components/ThemeButton.vue"
import ProgrammingLanguage from "@/components/ProgrammingLanguage.vue"

export default {
    name: "AboutView",
    components: {
        NavBar,
        BulletPoints,
        ThemeButton,
        ProgrammingLanguage
    },
    data() {
        return {
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
                {name: "Scala", rating: "two"},
                {name: "JavaScript", rating: "three"},
                {name: "PHP", rating: "two"},
                {name: "HTML", rating: "four"},
                {name: "CSS", rating: "four"},
                {name: "Shell", rating: "four"}
            ]
        }
    }
}
</script>

<style>
#about {
    margin-top: 150px
}

article h2 {
    margin-left: 100px;
    margin-top: 30px;
}

article p {
    margin: 30px 100px 0px 100px;
    font-size: 1.7em;
}
</style>