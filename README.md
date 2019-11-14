# assignment-05

ptm <- proc.time()
header <- read.table("A191RL1Q225SBEA.csv", header = TRUE,
                     sep=",", nrow = 1)
DF <- fread("A191RL1Q225SBEA.csv", skip=1, sep=",",
                  header=FALSE, data.table=FALSE)
setnames(DF, colnames(header))
rm(header)
FREAD_READ_TIME <- (proc.time() - ptm)
FREAD_READ_TIME