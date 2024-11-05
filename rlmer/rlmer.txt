# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Robust linear mixed models Use rlmer (robustlmm) With (In) R Software
install.packages("robustlmm")
library("robustlmm")
rlmer = read.csv("https://raw.githubusercontent.com/timbulwidodostp/rlmer/main/rlmer/rlmer.csv",sep = ";")
# Estimation Robust linear mixed models Use rlmer (robustlmm) With (In) R Software
## dropping of VC
system.time(rlmer(Yield ~ (1|Batch), rlmer))
## Default method "DAStau"
system.time(rfm.DAStau <- rlmer(Yield ~ (1|Batch), rlmer))
summary(rfm.DAStau)
## DASvar method
system.time(rfm.DASvar <- rlmer(Yield ~ (1|Batch), rlmer, method="DASvar"))
compare(rfm.DAStau, rfm.DAStau)
# Robust linear mixed models Use rlmer (robustlmm) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished