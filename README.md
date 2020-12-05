# BMB-Year-3-Project
Third Year Project R code for statistical analysis 


Code For R:

transformation_data <- read.csv(file.choose())

transformation_data

transformation <- stack(transformation_data)
names(transformation) <- c("Efficiency","Mutants")
transformation
transformationNoNA <- na.exclude(transformation)

transformationNoNA

p <- ggplot(transformationNoNA, aes(x=Mutants, y=Efficiency, fill = Mutants)) + 
  geom_boxplot() 
p
