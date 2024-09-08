# SGAN: Appliance signatures data generation for NILM applications using GANs

## Description
**[SGAN](https://link.springer.com/chapter/10.1007/978-3-031-62269-4_23)** is a GAN pipeline capable of producing power time series that resemble those observed in the real world, preserving the main characteristics and diversity of the observed electrical devices. Is it written on **[Pytorch](https://pytorch.org)** and **[Python](https://www.python.org)**.

The complementary paper "SGAN: Appliance signatures data generation for NILM applications using GANs" can be found [here](https://link.springer.com/chapter/10.1007/978-3-031-62269-4_23).

## Citation

In case you use SGAN to conduct research, please consider to cite our paper:

    @InProceedings{10.1007/978-3-031-62269-4_23,
    author="Gkoutroumpi, Christina
    and Gkalinikis, Nikolaos Virtsionis
    and Vrakas, Dimitrios",
    editor="Arai, Kohei",
    title="SGAN: Appliance Signatures Data Generation for NILM Applications Using GANs",
    booktitle="Intelligent Computing",
    year="2024",
    publisher="Springer Nature Switzerland",
    address="Cham",
    pages="325--339",
    abstract="The development and evolution of advanced energy system technologies is one of the most important goals for the global community in recent years. In this effort, the utilization and analysis of energy time series is of decisive importance for the understanding of energy consumption and production patterns. However, access to real data may be limited due to the sensitivity of the information and the limited amount of data already available. This has led to the use of methods to produce artificial data in order to enrich existing datasets. Generative Adversarial Networks or GANs are an approach to generative modeling using deep learning methods based on the logic of adversarial learning, and consist of two adversarial neural networks, a generator and a discriminator, which work together to produce realistic and unbiased data. The subject of the current paper is the creation of a GAN pipeline capable of producing power time series that resemble those observed in the real world, preserving the main characteristics and diversity of the observed electrical devices. The proposed method shows promising results, outperforming other state-of-the-art models in two calculated metrics.",
    isbn="978-3-031-62269-4"
    } = {10.3390/en15072647}
        }
    
For any enquiries, please contact the main authors.

## Library versions used

| Package    | Version |
| -------- | ------- |
| torch  | 2.0.1     |
| pandas | 1.5.3     |
| numpy    | 1.23.5   |
| matplotlib    | 3.7.1    |
| torchvision    | 0.15.2    |
| torchsummary    | 1.5.1    |
| wandb    | 0.15.10    |

## Datasets

The selected datasets include **UK DALE**[1], **REFIT**[2] and **Pecan Street**[3]
It should be noted that the data have to be downloaded manually.
In order to load the data, the files _path_manager.py_ and _datasource.py_ inside _datasources/_ directory should be 
modified accordingly.

## Run the project and train the models

In order to run the whole project and train the GAN, you should first obtain and store the data from one of the mentioned datasets.
Run the Notebook data_preprocess.ipynb first, to perform the first processing on the data of the chosen appliance. Set the paths on your computer, to save and load files appropriately.
After running the first notebook a pickle file will be created with the processed data.

The next step is to run the clean_dataset.ipynb file. This will read the pre processed data and performa the signature isolation and final cleaning of the data. Some plots and prints
are left in the code for debuggin purposes and to illustrate the process more clearly. After running this, the final signatures timeseries will be saved in pickle files.

Finally the last file sgan_train contains the main training loop and architectures of the models, as well the creation of the final timeseries. 

Please note that wandb is used in the final file for data visualization and keeping important information regarding the models and train process. If you do not wish to use it, you should 
remove it from the code.


## Licence

This project is licensed under the MIT License - see the [LICENSE](https://github.com/chrigkou/sgan/blob/main/LICENSE) file for details

## References
1. Jack, K.; William, K. The UK-DALE dataset domestic appliance-level electricity demand and whole-house demand from five UK
homes. Sci. Data 2015, 2, 150007.
2. Firth, S.; Kane, T.; Dimitriou, V.; Hassan, T.; Fouchal, F.; Coleman, M.; Webb, L. REFIT Smart Home dataset, 2017.
doi:10.17028/rd.lboro.2070091.v1.
3. Parson, Oliver, et al. "Dataport and NILMTK: A building data set designed for non-intrusive load monitoring." 2015 ieee global conference on signal and information processing (globalsip). IEEE, 2015.


