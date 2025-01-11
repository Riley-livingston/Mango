# Mango

Mango is an advanced trading card analysis platform that combines computer vision and metadata management to provide comprehensive card analysis, identification, and pricing.

## System Architecture

The Mango platform consists of two main components:

### [mango-metadata-api](https://github.com/yourusername/mango-metadata-api)
Backend service built with Node.js that manages and serves trading card metadata. This service provides:
- RESTful API for card metadata queries
- Database management for card information
- Metadata validation and processing
- Integration with custom card pricing APIs

### [mango-vision-pipeline](https://github.com/yourusername/mango-vision-pipeline)
Containerized computer vision pipeline that combines multiple models for card analysis:
- MMDet-based object detection for card identification
- Facebook's Segment Anything Model (SAM) for precise card segmentation
- Custom CNN for visual similarity search
- Docker-based deployment for easy scaling

## Getting Started

### Prerequisites
- Docker
- Node.js 18+
- Python 3.8+
- CUDA-compatible GPU (recommended)
- MySQL
### Installation

1. Clone the repositories:
```bash
git clone https://github.com/riley-livingston/mango-metadata-api
git clone https://github.com/riley-livingston/mango-vision-pipeline
```

2. Follow the individual setup instructions in each repository's README.

## System Flow

1. Images are submitted to the vision pipeline
2. Object detection identifies and localizes cards
3. SAM provides precise segmentation
4. Visual search identifies similar cards
5. Metadata API enriches results with card information

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

## License

This project is licensed under [Your chosen license] - see the [LICENSE](LICENSE) file for details.

## Contact

- GitHub: [@yourusername](https://github.com/rileylivingston)
- Project Link: https://github.com/yourusername/mango

## Acknowledgments

- Facebook Research for the SAM model
- MMDetection team
- Open source community
