Complete report: [BTPReport.pdf](https://github.com/surya-veer/Spectral-clustering-btp-project/files/9129831/BTPReport.pdf)
# Abstract
## Sampling and Clustering of Phenotypic and Genotypic  Soybean Dataset
Soybean forms an important cash crop for the Indian and French economy. It is the third
largest cultivated crop in India. In France, the amount of area being used for Soybean
farming is going up from 122,000 hectares in 2015 to about projected 200,000 hectares in
2020.
In the Indian context, we aim to develop a species of Soybean that is drought and heat

resistant (because of the erratic monsoons over this past decade) and in the French con-
text, we need to develop the species of Soybean that are resistant to flooding/too much

rainfall and extreme cold (because of increased frequency of arctic blasts happening
over the past many years). We break down our work in two parts. The first part deals
with the phenotypic data and finds correlations between different phenotypic factors.

Using this phenotypic data, we also cluster plants with similar phenotypic features to-
gether and then finally, take the best species out of each cluster. We have then also

applied pivotal sampling techniques to reduce the dimensionality of the data.
Basically, this project can be divided into the following parts:
- Correlations between several phenotypic factors
- Spectral clustering to cluster plants based on their phenotypic properties
- Sampling of the whole genome sequence of soybean to reduce the dimensionality
of the data using Pivotal Sampling
- Clustering of sampled whole genome sequences using Spectral Clustering

## 1.1 About Phenotypic Data
A phenotype is the composite of an organism’s observable characteristics or traits, such
as its morphology, development, biochemical or physiological properties, behavior, and

products of behavior (such as a bird’s nest). In context of Soybean, we have been pro-
vided a phenotypic data set that has observable characteristics of many different species

of Soybean plant. We were given several properties mapped to a specific species. For eg,
early plant vigour, Hypocotyl color, stem determination, days to 50% flowering, flower
color, leaf shape, leaflet color, number of leaflets, seed yield per plant, 100 seed weight
and many more.

## 1.2 About some phenotypic properties of Soybean plant
- Early plant vigour: The strength of plant in its early days.
- Hypocotyl color: The part of the stem of an embryo plant beneath the stalks of the
seed leaves or cotyledons and directly above the root is Hypocotyl.
- Days to 50% flowering
- Flower Color
- Leaf Shape and color
- Number of Leaflets
- Pubescence: Fine short hair on plant stem - present or not. It’s color and density,
type (erect, semi-appressed etc) are other related properties.
- Plant height, Number of Primary and Secondary Branches.

- Lodging: the displacement of stems or roots from their vertical and proper place-
ment.

# Literature Review

There has been a lot of research ongoing in the field of genomics and a lot of efforts are

being made to attain better accuracy to map the phenotypic and the genomic character-
istics. As in this part, we dealt only with the phenotypic data so the chapter discusses

literature pertaining to previously known methods of finding correlations among sev-
eral factors and about spectral clustering.

## Spectral Clustering
Clustering is one of the most widely used techniques for exploratory data analysis, with

applications ranging from statistics, computer science, biology to social sciences or psy-
chology. In virtually every scientific field dealing with empirical data, people attempt

to get a first impression on their data by trying to identify groups of “similar behavior”

in their data. Compared to the “traditional algorithms” such as k-means or single link-
age, spectral clustering has many fundamental advantages. Results obtained by spectral 
clustering often outperform the traditional approaches, spectral clustering is very sim-
ple to implement and can be solved efficiently by standard linear algebra methods. [6]

The spectral clustering method can basically be divided in three parts:
### 1. Constructing the similarity graph
Constructing the similarity graph for spectral clustering is not a trivial task, and little is
known on theoretical implications of the various constructions.
<img width="582" alt="image" src="https://user-images.githubusercontent.com/20180313/179455806-2c08d647-f554-493b-8702-6de4086d323c.png">

### 2.How to compute the eigenvectors?
Now, let k be the number of clusters that we have decided to make. To implement
spectral clustering in practice one has to compute the first k eigenvectors of a potentially large graph Laplace matrix. Luckily, if we use the k-nearest neighbor graph or
the e-neighborhood graph, then all those matrices are sparse. Efficient methods exist
to compute the first eigenvectors of sparse matrices, the most popular ones being the
power method or Krylov subspace methods such as the Lanczos method[7]. The speed
of convergence of those algorithms depends on the size of the eigengap (also called
spectral gap). The larger this eigengap is, the faster the algorithms computing the first
k eigenvectors converge.
Note that a general problem occurs if one of the eigenvalues under consideration has
multiplicity larger than one. For example, in the ideal situation of k disconnected clusters, the eigenvalue 0 has multiplicity k. As we have seen, in this case the eigenspace
is spanned by the k cluster indicator vectors. But unfortunately, the vectors computed
by the numerical eigensolvers do not necessarily converge to those particular vectors.
Instead they just converge to some orthonormal basis of the eigenspace, and it usually
depends on implementation details to which basis exactly the algorithm converges.

### 3. The K-means step
K-means is the last step for the sprectral clustering algorithm. This step is used to take
out the final partition from the real-valued matrix of eigenvectors obtained in the step
above.
While it is somewhat arbitrary what clustering algorithm exactly one chooses in the
final step of spectral clustering, one can argue that at least the Euclidean distance between the points yi
is a meaningful quantity to look at. We have seen that the Euclidean
distance between the points yi
is related to the “commute distance” on the graph, and in
Nadler, Lafon, Coifman, and Kevrekidis (2006) [8] the authors show that the Euclidean
distances between the yi are also related to a more general “diffusion distance”.

# Analysis of different phenotypic factors
 Pearson Correlation Coefficients for Phenotypic Traits
- The Pearson correlation coefficient is just one of many types of correlation coefficients in the field of statistics.
- In order to determine how strong the relationship is between two variables, a formula must be followed to produce what is referred to as the coefficient value.
- The coefficient value can range between -1.00 and 1.00. If the coefficient value is
in the negative range, then that means the relationship between the variables is
negatively correlated, or as one value increases, the other decreases. If the value
is in the positive range, then that means the relationship between the variables is
positively correlated, or both values increase or decrease together.
- To find correlation between  x and y:
<img width="257" alt="Screenshot 2022-07-18 at 12 04 20 PM" src="https://user-images.githubusercontent.com/20180313/179456242-a19e553f-ad40-4bdd-8d93-edfcc9fc0655.png">

Where x and y are any two columns and i is the row number.

[READ more](https://github.com/surya-veer/Spectral-clustering-btp-project/blob/main/BTPReport.pdf)

