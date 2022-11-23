# Prediction of antimicrobial peptide against enteric pathogens

Abstract: Specific targeted antimicrobial peptides (STAMPs) are novel alternatives to antibiotics for killing target pathogens without damaging commensal bacteria, thereby avoiding antibiotic-associated dysbiosis and bacterial resistance. However, limited de novo designs efficiency, colonic bioavailability, and delivery systems restrict the development of STAMPs for colonic infections. In this study, we report a simple and efficient de novo STAMP design strategy that combines a traversal design, machine learning model and phage display technology to identify STAMPs against Clostridium perfringens. STAMPs could damage the capsule, cell wall, and membrane of C. perfringens and self-assemble into nanonetworks to entrap pathogens and eliminate biofilms. We also designed a gut-targeted engineered particle vaccine (EPV) for STAMP delivery. Our in vivo results showed that both STAMP and EPV@STAMP limited C. perfringens overgrowth, colon invasion, and translocation and reduced the levels of pro-inflammatory cytokines and toxins in serum and colonic tissue; furthermore, EPV@STAMP had a stronger colonic protection ability than STAMP alone. Moreover, 16S rRNA sequencing revealed that STAMPs could significantly increase community richness compared with broad-spectrum antimicrobial peptides and that both STAMPs and EPV@STAMP promoted the recovery of disturbed gut microflora. The results indicate that EPV@STAMP is a promising candidate for the treatment of Clostridium infections. Our STAMP screening strategy can accelerate the development of precise antimicrobials and their delivery. 

The DBAASP database was used to construct a dataset for ML model. Monomeric AMPs without unusual amino acids and bonds and with known minimum inhibitory concentration (MIC) for enteric pathogens were screened out. In total, 1,621 AMPs were considered, and the AMPs were divided into three groups: high (0 μg/ml <MIC≤32 μg/ml), low (32 μg/ml<MIC≤128 μg/ml), and no (MIC>128 μg/ml) activities. After the oversampling algorithm was used to balance the samples in each class, we randomly split the dataset into 80% training data and 20% test data. AutoGluon was used to establish the ML prediction models. A total 26 models with 10-fold cross-validation were tested, of which WeightedEnsemble_L3 provided the best performance (table S1). This model achieved a receiver operating characteristic curve-area under the curve (ROC-AUC) of 0.912 on the test data (Fig. 1B,C). Using inactive peptides as the external test set, the prediction accuracy reached 90%.
PS:The code is completely executed according to AutoGluon's reference case (https://auto.gluon.ai/stable/tutorials/tabular_prediction/index.html), no additional revisions have been conducted.


