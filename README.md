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

## Datasets

The selected datasets include **UK DALE**[1], **REFIT**[2] and **Pecan Street**[3]
It should be noted that the data have to be downloaded manually.
In order to load the data, the files _path_manager.py_ and _datasource.py_ inside _datasources/_ directory should be 
modified accordingly.

## Licence

This project is licensed under the MIT License - see the [LICENSE]() file for details

## References
1. Jack, K.; William, K. The UK-DALE dataset domestic appliance-level electricity demand and whole-house demand from five UK
homes. Sci. Data 2015, 2, 150007.
2. Firth, S.; Kane, T.; Dimitriou, V.; Hassan, T.; Fouchal, F.; Coleman, M.; Webb, L. REFIT Smart Home dataset, 2017.
doi:10.17028/rd.lboro.2070091.v1.
3. Parson, Oliver, et al. "Dataport and NILMTK: A building data set designed for non-intrusive load monitoring." 2015 ieee global conference on signal and information processing (globalsip). IEEE, 2015.

