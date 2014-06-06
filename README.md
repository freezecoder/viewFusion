viewFusion
==========
Not act his is my fork of something. View fusion event by [circos](http://circos.ca/) plot. I will support multiple formats generated by 
different fusion dicovery softwares in future. Currently it has only implemented parsing results 
coming from [FusionHunter](http://bioen-compbio.bioen.illinois.edu/FusionHunter/) program.

Some new data
Usage
----------------
```
perl viewFusion.pl -i/--input <inputFusionResult> -f/--format [fusionResultFormat] -s/--species [human] -b/--build [hg19]
   
     -i/--input   fusion result file from fusion detecting program(e.g, FusionHunter)
     -f/--format  the format of the fusion result, use program name as it format, default is FusionHunter
     -s/--species which species's karyotype will be use in the plot(e.g,human,mouse),default is human
     -b/--build   which version(e.g., hg19,mm8,mm9),default is hg19
     -h/--help    print out this help
     -l/--list    list current supported species' karyotypes in karyotype folder,then exists
```

Example
----------------------
In the 'Example' sub-folder, there is an example of fusion result coming from FusionHunter. 
It combines contents in the ***FusionHunter.fusion*** and ***FusionHunter.readthrough*** files. According to the author,
***FusionHunter.readthrough*** is fusion genes linking two adjacent genes on chromosome, while 
***FusionHunter.fusion*** reports fusion genes from distinct genomic regions.

Code:
```
../viewFusion.pl -i FusionHunter.result
```

Support for more tools
----------------------
Chimerascan


Result:

![example plot](https://github.com/riverlee/viewFusion/raw/master/Example/circos-fusion.png)
