# 🎉 RAG Frameworks for ARM64 🎉

**Welcome to the RAG Frameworks for ARM64 repository!** 🌟

This project offers a customized setup of the RAG frameworks, specifically designed for the ARM64 architecture. Due to the absence of official ARM64 support, we have taken the initiative to compile ragflow and rewrite the Docker Compose configuration based on the official repository. Additionally, we have replaced the original official images with those from changsha-aicc to achieve two main objectives: 
1. Adaptation to the ARM64 environment for the ragflow image 🛠️; 
2. Network acceleration in domestic environments for other images 🚀.

## Getting Started 🚀

### Prerequisites 📋

- Docker >= 24.0.0 & Docker Compose >= v2.26.1

### Installation 🛠️

1. **Clone the Repository** 

   ```bash
   git clone https://github.com/xiaoloongfang/rag-frameworks-for-arm64.git
   ```

2. **Run the Containers**

   Use the following command to start the services:

   ```bash
   cd rag-frameworks-for-arm64/ragflow
   docker-compose -f docker-compose.yml up -d
   ```

    The ragflow server are up and running.

### Configuration ⚙️

For configuration options, check out the [ragflow repo](https://github.com/infiniflow/ragflow/tree/main).

### Replaced Container Images 🚢

We've given the following container images with changsha-aicc versions:

- Ragflow (adapted for ARM64): `swr.cn-central-232.csai.hunan.com.cn/changsha-aicc/ragflow-slim:v0.16.0-arm64`
- Elasticsearch (for network acceleration): `swr.cn-central-232.csai.hunan.com.cn/changsha-aicc/elasticsearch:8.11.3`
- Infinity (for network acceleration): `swr.cn-central-232.csai.hunan.com.cn/changsha-aicc/infiniflow/infinity:v0.6.0-dev3`
- MySQL (for network acceleration): `swr.cn-central-232.csai.hunan.com.cn/changsha-aicc/mysql:8.0.39`
- MinIO (for network acceleration): `swr.cn-central-232.csai.hunan.com.cn/changsha-aicc/minio:RELEASE.2023-12-20T01-00-02Z`
- Redis (for network acceleration): `swr.cn-central-232.csai.hunan.com.cn/changsha-aicc/valkey:8`

## Future Plans 🌟

- Add Docker Compose configurations for additional repositories like Dify.

## Contributing 🤝

Contributions are welcome! Please feel free to submit a Pull Request.

## License 📜

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For any inquiries, please contact [xiaoloongfang@gmail.com](mailto:xiaoloongfang@gmail.com).
