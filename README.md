# Mango

Mango is an open-source comprehensive trading card platform that combines computer vision analysis, metadata management, and collection tracking capabilities to provide a complete solution for card collectors and investors.

## System Architecture

The Mango platform consists of three main components:

### [mango-client](https://github.com/riley-livingston/mango-client)
A sophisticated web application for collectors that provides:
- Custom collection creation and management
- Granular card filtering and organization
- Price tracking and analytics
- Portfolio value monitoring
- Integration with vision pipeline for card identification
- User-defined collection categories and tracking parameters

### [mango-metadata-api](https://github.com/riley-livingston/mango-metadata-api)
Backend service built with Node.js that manages and serves trading card metadata. This service provides:
- RESTful API for card metadata queries
- Database management for card information
- Metadata validation and processing
- Integration with card pricing APIs
- User collection data management
- Price history tracking

### [mango-vision-pipeline](https://github.com/riley-livingston/mango-vision-pipeline)
Containerized computer vision pipeline that combines multiple models for card analysis:
- MMDet-based object detection for card identification
- Facebook's Segment Anything Model (SAM) for precise card segmentation
- Custom CNN for visual similarity search
- Docker-based deployment for easy scaling

## System Flow

1. Users can build collections through:
   - Manual card entry with granular details
   - Images processed by the vision pipeline
2. The vision pipeline processes uploaded images:
   - Object detection identifies and localizes cards
   - SAM provides precise segmentation
   - Visual search identifies similar cards
3. Metadata API enriches results with:
   - Detailed card information
   - Current market prices
   - Historical price data
4. Users can:
   - Track collection value
   - Monitor price changes
   - Create custom sets and track completion
## Getting Started

### Prerequisites
- Docker and Docker Compose
- Node.js 18+
- Python 3.8+
- MySQL
- CUDA-compatible GPU (recommended)

### Installation

1. Clone the repositories:
```bash
git clone https://github.com/riley-livingston/mango-client
git clone https://github.com/riley-livingston/mango-metadata-api
git clone https://github.com/riley-livingston/mango-vision-pipeline
```

2. Follow the individual setup instructions in each repository's README.

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

## License

This project is licensed under [Your chosen license] - see the [LICENSE](LICENSE) file for details.

## Contact

- GitHub: [@yourusername](https://github.com/riley-livingston)
- Project Link: https://github.com/riley-livingston/mango

## Acknowledgments

- Facebook Research for the SAM model
- MMDetection team
- Open source community
