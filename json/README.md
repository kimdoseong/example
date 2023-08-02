# boost
git clone https://boostorg.jfrog.io/artifactory/main/release/1.82.0/source/boost_1_82_0.tar.gz \
tar -xvf boost_1_82_0.tar.gz \
cd boost_1_82_0.tar.gz \
./bootstrap.sh \
sudo  ./b2 install \

# nlohmann
git clone https://github.com/nlohmann/json.git \
sudo cp -r json/include/nlohmann/ /usr/local/include/ \