# If you want to use this container, it is simpler to just pull it:
#   docker pull leandroishilima/mobmess:0.0.1
# to build: docker build . -t leandroishilima/mobmess:0.0.1
FROM continuumio/miniconda3:4.12.0

RUN /opt/conda/bin/conda install -y -c anaconda -c conda-forge -c bioconda --override-channels --strict-channel-priority  numpy pandas scipy scikit-learn igraph numba python-blosc mummer4
RUN git clone https://github.com/michaelkyu/PlasX.git && pip install ./PlasX
RUN git clone https://github.com/leoisl/MobMess.git && pip install ./MobMess
RUN mobmess -h
