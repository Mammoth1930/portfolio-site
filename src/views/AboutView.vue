<template>
    <NavBar/>
    <section id="about">
        <article>
            <h2>Overview</h2>
            <p>
                I’m a very hard-working, motivated and personable data professional, who recently graduated from one of Australia’s highest-ranking universities, The University of Queensland, with a bachelor's degree in Computer Science. While completing this degree I fell in love with the theory and concepts of relational databases, artificial intelligence, and machine learning and as a result, chose Data Science as the major for my degree. While studying I also chose to work casually at the university by helping to teach and develop content for a first-year <a href="https://my.uq.edu.au/programs-courses/course.html?course_code=INFS1200" target="_blank" rel="noopener noreferrer">course</a> on relational databases and SQL. During my time at university, I was able to learn about and use many different data-driven concepts and tools including:
                
                <BulletPoints :points="dataScienceConcepts" id="dataScienceConcepts"/>
            </p>
            <ThemeButton/>
        </article>


    </section>

</template>

<script>
import NavBar from "@/components/NavBar.vue"
import BulletPoints from "@/components/BulletPoints.vue"
import ThemeButton from "@/components/ThemeButton.vue"

export default {
    name: "AboutView",
    components: {
        NavBar,
        BulletPoints,
        ThemeButton
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