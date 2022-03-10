# code :1.1  line chart
corr <- round(cor(deathdata1[,2:5]), 1)
ggcorrplot(corr, hc.order = TRUE, 
           type = "lower", 
           lab = TRUE, 
           lab_size = 5, 
           colors = c("#6D9EC1", "white", "#E46726"), 
           title="Correlogram of data in uk", 
           ggtheme=ggplot2::theme_gray)
