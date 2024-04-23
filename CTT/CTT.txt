# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Classicial Test Theory Item Analysis for Multiple Choice Test Items Use Package CTT With (In) R Software
install.packages("CTT")
library("CTT")
# Import Data Excel Into R From Github Olah Data Semarang (timbulwidodostp)
exam_data<-read.csv("https://github.com/timbulwidodostp/CTT/raw/main/CTT/CTT.csv",sep = ";")
# Estimate Classicial Test Theory Item Analysis for Multiple Choice Test Items Use Package CTT With (In) R Software
items_only<-exam_data[,1:56]
exam_key<-c("A","D","C","B","C","B","C","D","A","D","C","A","D","C","A",
"B","D","B","A","C","A","A","C","B","C","B","D","A","A","A",
"C","B","B","A","B","D","D","A","D","C","D","A","B","B","C",
"D","B","C","C","B","D","A","C","B","A","D")
exam_score<-score(items_only, key=exam_key, output.scored=TRUE, rel=TRUE)
report<-itemAnalysis(exam_score$scored, itemReport=TRUE)
report[["itemReport"]]
# Classicial Test Theory Item Analysis for Multiple Choice Test Items Use Package CTT With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
