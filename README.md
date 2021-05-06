# Detailed Description of this files


### Gene expression file：

+ `test_gene_expression.bed.gz`
+ `test_gene.txt` gene location file

### genoType file：

1. `test_genotype.vcf` 
2. `test_plink` plink file

### cis mapping file:

1. `test_cis_permute.txt`

### covariates file:

1. `covariates.txt`

### independent cis-QTL out file:

1. `independ_out.cis_independent_qtl.txt.gz`
2. `independ_out.tensorQTL.cis_independent.log`

## the command I used:

```bash
# change vcf to plink
plink --make-bed --output-chr 26 -vcf test_genotype.vcf -out test_plink
# independ eQTL analysis
python -m tensorqtl test_plink  test_gene_expression.bed.gz independ_out --covariates  covariates.txt  --cis_output test_cis_permute.txt  --mode cis_independent
```
## Software version
```bash
Python 3.6.5 
Package                           Version
--------------------------------- ----------
absl-py                           0.12.0
ansiwrap                          0.8.4
appdirs                           1.4.4
argon2-cffi                       20.1.0
astor                             0.8.1
astunparse                        1.6.3
async-generator                   1.10
attrs                             20.3.0
autopep8                          1.5.3
backcall                          0.2.0
backports.lzma                    0.0.14
bash-kernel                       0.7.2
beautifulsoup4                    4.7.1
bgionline                         3.0.3
bio                               0.1.0
biopython                         1.74
black                             20.8b1
bleach                            3.3.0
blessings                         1.6
boto3                             1.4.6
botocore                          1.6.8
bx-python                         0.8.11
cached-property                   1.5.2
cachetools                        4.2.1
certifi                           2019.11.28
cffi                              1.14.5
chardet                           3.0.4
click                             7.1.2
colourmap                         0.1.1
crcmod                            1.7
cycler                            0.10.0
Cython                            0.29.14
dask                              2021.3.0
dataclasses                       0.8
decorator                         4.4.2
defusedxml                        0.7.1
Deprecated                        1.2.12
docutils                          0.15.2
entrypoints                       0.3
fasteners                         0.16
fsspec                            2021.4.0
gast                              0.3.3
google-auth                       1.27.1
google-auth-oauthlib              0.4.3
google-pasta                      0.2.0
gpflow                            1.3.0
grpcio                            1.36.1
h5py                              2.10.0
idna                              2.6
importlib-metadata                3.7.3
iniconfig                         1.1.1
ipykernel                         5.5.0
ipython                           7.16.1
ipython-genutils                  0.2.0
jedi                              0.17.2
Jinja2                            2.11.3
jmespath                          0.9.4
joblib                            1.0.1
jsonschema                        3.2.0
jupyter-client                    6.1.12
jupyter-contrib-core              0.3.3
jupyter-contrib-nbextensions      0.5.1
jupyter-core                      4.7.1
jupyter-highlight-selected-word   0.2.0
jupyter-latex-envs                1.4.6
jupyter-nbextensions-configurator 0.4.1
jupyterlab-pygments               0.1.2
Keras-Applications                1.0.8
Keras-Preprocessing               1.1.2
kiwisolver                        1.2.0
locket                            0.2.1
lxml                              4.6.3
Markdown                          3.3.4
MarkupSafe                        1.1.1
matplotlib                        3.2.1
matplotlib-venn                   0.11.5
metakernel                        0.27.5
mistune                           0.8.4
mock                              4.0.3
multipledispatch                  0.6.0
mypy-extensions                   0.4.3
nbclient                          0.5.3
nbconvert                         6.0.7
nbformat                          5.1.2
nest-asyncio                      1.5.1
networkx                          2.5.1
notebook                          6.3.0
numexpr                           2.7.3
numpy                             1.19.5
oauthlib                          3.1.0
opt-einsum                        3.3.0
oss2                              2.3.4
packaging                         20.9
pandas                            1.1.3
pandas-plink                      2.2.4
pandocfilters                     1.4.3
papermill                         2.3.3
parso                             0.7.1
partd                             1.2.0
pathspec                          0.8.1
patsy                             0.5.1
pca                               1.4.0
pexpect                           4.8.0
pickleshare                       0.7.5
pip                               21.0.1
pluggy                            0.13.1
prometheus-client                 0.9.0
prompt-toolkit                    3.0.17
protobuf                          3.15.6
psutil                            5.4.1
ptyprocess                        0.7.0
py                                1.10.0
pyarrow                           3.0.0
pyasn1                            0.4.8
pyasn1-modules                    0.2.8
pyBigWig                          0.3.18
pycodestyle                       2.6.0
pycparser                         2.20
pydot                             1.4.2
pydotplus                         2.0.2
Pygments                          2.8.1
pyparsing                         2.4.7
pyreadline                        2.1
pyrsistent                        0.17.3
pysam                             0.16.0.1
pytest                            6.2.2
python-dateutil                   2.8.1
pytz                              2019.2
PyYAML                            5.4.1
pyzmq                             22.0.3
qtl                               0.1.8
regex                             2021.4.4
requests                          2.25.1
requests-oauthlib                 1.3.0
rpy2                              3.4.3
rsa                               4.7.2
s3transfer                        0.1.13
scikit-learn                      0.24.1
scipy                             1.4.1
seaborn                           0.11.1
Send2Trash                        1.5.0
setuptools                        54.1.2
six                               1.15.0
sklearn                           0.0
sos                               0.22.5
sos-bash                          0.20.0
sos-notebook                      0.22.4
sos-papermill                     0.2.1
sos-python                        0.18.4
sos-r                             0.19.6
soupsieve                         1.9.2
statsmodels                       0.10.1
tables                            3.6.1
tabulate                          0.8.9
tenacity                          7.0.0
tensorboard                       1.13.1
tensorflow                        1.13.1
tensorflow-estimator              1.13.0
tensorqtl                         1.0.5
termcolor                         1.1.0
terminado                         0.9.4
testpath                          0.4.4
textwrap3                         0.9.2
threadpoolctl                     2.1.0
toml                              0.10.1
toolz                             0.11.1
torch                             1.8.1
tornado                           6.1
tqdm                              4.60.0
traitlets                         4.3.3
typed-ast                         1.4.3
typing-extensions                 3.7.4.3
tzlocal                           2.1
urllib3                           1.22
wcwidth                           0.2.5
webencodings                      0.5.1
Werkzeug                          1.0.1
wget                              3.2
wheel                             0.35.1
wrapt                             1.12.1
xarray                            0.16.2
xxhash                            2.0.2
zipp                              3.4.1
zstandard                         0.15.2

```
