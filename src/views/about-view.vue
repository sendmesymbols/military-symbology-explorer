<template>
    <div class="container">
        <div class="row">

            <div class="col-sm-10 main">
                <h1 class="page-header">About</h1>

                <p>The joint military symbology explorer is an experiment created primarily for</p>
                <ul>
                    <li>learning the <a
                        href="https://github.com/Esri/joint-military-symbology-xml">Joint Military Symbology Markup
                        Language
                        (JMSML)</a></li>
                    <li>experimenting with Javascript frameworks and tools</li>
                </ul>
                <p>The JMSML project is an initiative by <a href="http://www.esri.com/">Esri</a>, and provides
                    a data encapsulation of <a
                        href="http://www.assistdocs.com/search/document_details.cfm?ident_number=114934">MIL-STD-2525D</a>
                    and <a href="http://en.wikipedia.org/wiki/NATO_Military_Symbols_for_Land_Based_Systems">APP-6(C)</a>.
                </p>

                <p>If you find bugs or have ideas for improving the symbology explorer, feel free to <a
                    href="https://github.com/kjellmf">contact me</a> or submit an
                    issue on the <a
                        href="https://github.com/kjellmf/military-symbology-explorer">GitHub project page</a>. </p>

                <h2>Licensing and copyright</h2>

                <p>JMSML schema and instance data: Copyright 2014 Esri</p>

                <p>Symbol SVG files: Copyright 2014 DISA (SSMC Technical Working Group).</p>

                <p>The source code for the symbology explorer is <a
                    href="https://github.com/kjellmf/military-symbology-explorer">available on GitHub</a>
                    under the Apache 2 license.</p>

                <h2>Technical details</h2>

                <p>All of the symbol definitions and symbol SVG files are from the <a
                    href="https://github.com/Esri/joint-military-symbology-xml">JMSML project</a>.
                    I have just converted the data to a Javascript-friendly format and assembled the different SVG files
                    into symbols.</p>

                <p>
                    Please note that the symbology explorer is an experiment. I don't recommend using the techniques I have
                    used in production for the
                    following reasons:</p>

                <ul>
                    <li>Almost all of the JMSML data is loaded into memory (see <a
                        href="https://github.com/kjellmf/military-symbology-explorer/blob/master/data/jmsml.js">jmsml.js</a>)
                        when the page is loaded. Unless you are writing a symbology explorer this approach is a waste of
                        memory.
                    </li>
                    <li>
                        Drawing a symbol requires up to six different SVGs (and many server request). In a production system
                        combine the SVGs on the server and send only one SVG file to the client.
                    </li>
                </ul>


                <p>Some tools and frameworks I have used for this project:</p>

                <ul>
                    <li><a href="https://www.python.org/">Python (2.7)</a> for extracting information from the <a
                        href="https://github.com/Esri/joint-military-symbology-xml/tree/master/instance">JMSML instance
                        files</a> and
                        converting it to javascript
                    </li>

                    <li><a href="http://getbootstrap.com/">Bootstrap</a>
                        for styling (I'm sorry for using the default styles
                        )
                    </li>

                </ul>

                <h2>Related projects</h2>

                <p>
                    JMSML is not the only open source symbology project. If you need a symbol renderer check out one of these
                    projects:</p>
                <ul>
                    <li><a href="https://github.com/missioncommand/mil-sym-js">mil-sym-js</a>
                        MIL-STD-2525 symbol rendering
                        JavaScript library for modern web applications (font based, 2525B, 2525C)
                    </li>
                    <li><a href="https://github.com/missioncommand/mil-sym-java">mil-sym-js</a> MIL-STD-2525 B and C
                        rendering library and web service
                    </li>
                    <li><a href="https://github.com/spatialillusions/MilSymbol">MilSymbol</a> Military Unit Symbols in
                        JavaScript (SVG based, APP6B, 2525C)
                    </li>
                    <li><a href="https://github.com/StackFrame/Ortelium">Ortelium</a> A tool for generating military map
                        symbols (Java, 2525B)
                    </li>
                    <li><a href="http://milsym.codeplex.com/">MilSym</a>
                        Provides C# WPF & Silverlight 4.0, XAML-based, Bing
                        & Esri map symbology (2525C)
                    </li>
                </ul>

            </div>
        </div>
    </div>


</template>

<script lang="ts">
    import Vue from 'vue';
    import {Component} from 'vue-property-decorator';

    @Component
    export default class AboutView extends Vue {
    }
</script>

<style scoped>


</style>
