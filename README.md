# 🤖 AI API Testing Framework

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://www.python.org/)
[![Pytest](https://img.shields.io/badge/Testing-Pytest-green.svg)](https://pytest.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Tests](https://img.shields.io/badge/Tests-14%20Passed-success.svg)](tests/)

Comprehensive API testing framework for AI/ML applications with focus on quality assurance, performance validation, and automated testing.

## 🎯 Purpose

This framework demonstrates professional API testing practices for AI/ML systems, including:
- ✅ Functional testing of API endpoints
- ✅ Response validation and structure verification
- ✅ Performance and load testing
- ✅ Error handling and edge case testing
- ✅ Automated test reporting

## 🛠️ Technologies Used

- **Python 3.9+** - Core programming language
- **Pytest** - Testing framework with fixtures and parametrization
- **Requests** - HTTP library for API calls
- **unittest.mock** - Mock testing for isolated unit tests
- **pytest-html** - HTML test report generation
- **pytest-cov** - Code coverage reporting

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/miramamdoh23/ai-api-testing-framework.git
cd ai-api-testing-framework

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## 🚀 Quick Start

```bash
# Run all tests
pytest tests/ -v

# Run with coverage report
pytest --cov=tests tests/

# Generate HTML report
pytest --html=reports/test_report.html tests/

# Run specific test class
pytest tests/test_api_endpoints.py::TestAIAPIEndpoints -v

# Run with print statements visible
pytest tests/ -v -s
```

## 📊 Test Coverage

| Test Category | Coverage | Status |
|--------------|----------|--------|
| API Endpoints | 100% | ✅ Pass |
| Error Handling | 100% | ✅ Pass |
| Model Validation | 100% | ✅ Pass |
| **Overall** | **100%** | **✅ Pass** |

## 🧪 Test Results

✅ **All 14 tests passing successfully!**

```bash
======================== 14 passed in 0.60s ========================
```

### Test Breakdown:
- ✅ **8 API Endpoint Tests** - AI model responses, text generation, sentiment analysis
- ✅ **4 Error Handling Tests** - 404, 400, 401, 429 status codes
- ✅ **2 Model Validation Tests** - Token limits, confidence scores

### Test Categories:

| Category | Tests | Description |
|----------|-------|-------------|
| **API Connectivity** | 1 | Basic endpoint availability testing |
| **Response Structure** | 1 | JSON structure and field validation |
| **Performance** | 1 | Response time < 2 seconds SLA |
| **Model Parameters** | 3 | Different AI models (GPT-4, GPT-3.5, invalid) |
| **AI Generation** | 2 | Text generation & sentiment analysis |
| **Error Handling** | 4 | HTTP status codes (400, 401, 404, 429) |
| **Model Validation** | 2 | Token limits & confidence scores |

### Skills Demonstrated:
- ✅ Mock testing for AI/ML APIs
- ✅ pytest framework proficiency
- ✅ API response validation
- ✅ Error handling verification
- ✅ Performance testing (response time < 2s)
- ✅ Parametrized testing
- ✅ Professional test documentation

## 🧪 Example Test Output

```bash
tests/test_api_endpoints.py::TestAIAPIEndpoints::test_api_connectivity PASSED [  7%]
✅ API Connectivity Test PASSED

tests/test_api_endpoints.py::TestAIAPIEndpoints::test_ai_model_response_structure PASSED [ 14%]
✅ Response Structure Test PASSED

tests/test_api_endpoints.py::TestAIAPIEndpoints::test_response_time_performance PASSED [ 21%]
✅ Response Time Test PASSED: 0.80s

tests/test_api_endpoints.py::TestAIAPIEndpoints::test_ai_text_generation PASSED [ 50%]
✅ AI Text Generation Test PASSED

tests/test_api_endpoints.py::TestAIAPIEndpoints::test_sentiment_analysis_api PASSED [ 57%]
✅ Sentiment Analysis Test PASSED

tests/test_api_endpoints.py::TestErrorHandling::test_invalid_endpoint_404 PASSED [ 64%]
✅ 404 Error Handling Test PASSED

tests/test_api_endpoints.py::TestErrorHandling::test_rate_limit_error_429 PASSED [ 85%]
✅ 429 Rate Limit Test PASSED

tests/test_api_endpoints.py::TestAIModelValidation::test_confidence_score_range PASSED [100%]
✅ Confidence Score Range Test PASSED
```

## 💡 Key Features

### 1. **Automated Testing**
- Comprehensive test suites for API validation
- Parameterized tests for multiple scenarios
- Automated regression testing capability

### 2. **Quality Assurance**
- Response structure validation
- Performance benchmarking (< 2s SLA)
- Edge case and error scenario testing

### 3. **Mock Testing Implementation**
- No external API dependencies
- Fast test execution
- Controlled test scenarios
- Isolated unit testing

### 4. **Detailed Reporting**
- HTML test reports with pytest-html
- Coverage metrics tracking
- Performance analytics
- Clear pass/fail indicators

## 📁 Project Structure

```
ai-api-testing-framework/
│
├── tests/                      # Test suites
│   ├── __init__.py            # Package initialization
│   └── test_api_endpoints.py  # Main API tests
│
├── utils/                      # Helper utilities (future)
│   ├── api_client.py          # API client wrapper
│   └── validators.py          # Response validators
│
├── config/                     # Configuration files (future)
│   └── test_config.yaml       # Test settings
│
├── reports/                    # Generated test reports
│   └── test_results.html      # HTML reports
│
├── requirements.txt            # Python dependencies
├── .gitignore                 # Git ignore rules
└── README.md                   # This file
```

## 🎓 Skills Demonstrated

### Technical Skills:
- ✅ **API Testing** - REST API validation and testing
- ✅ **Test Automation** - pytest framework and fixtures
- ✅ **Python Programming** - Clean, maintainable code
- ✅ **Mock Testing** - unittest.mock for isolated tests
- ✅ **Quality Assurance** - Comprehensive test coverage
- ✅ **Performance Testing** - Response time validation
- ✅ **Error Handling** - Multiple HTTP status code scenarios

### Professional Skills:
- ✅ **Test Documentation** - Clear, professional README
- ✅ **Version Control** - Git and GitHub workflow
- ✅ **Best Practices** - PEP 8, type hints, docstrings
- ✅ **CI/CD Ready** - Easy integration with pipelines

## 🔧 Future Enhancements

- [ ] Add CI/CD pipeline with GitHub Actions
- [ ] Implement pytest fixtures in conftest.py
- [ ] Add load testing with concurrent requests
- [ ] Create API client wrapper utility
- [ ] Add response time trend analysis
- [ ] Implement test data generators
- [ ] Add integration with real AI APIs (OpenAI, Hugging Face)

## 📝 Test Examples

### Testing AI Model Response
```python
@patch('requests.post')
def test_ai_text_generation(self, mock_post):
    """Test AI text generation endpoint"""
    mock_post.return_value = MockResponse(
        json_data={
            "prompt": "What is machine learning?",
            "generated_text": "Machine learning is a subset of AI...",
            "model": "gpt-4"
        },
        status_code=201
    )
    
    response = requests.post(f"{self.BASE_URL}/generate", json=payload)
    assert response.status_code == 201
    assert "generated_text" in response.json()
```

### Testing Error Handling
```python
@patch('requests.post')
def test_invalid_parameters_400(self, mock_post):
    """Test 400 bad request error"""
    mock_post.return_value = MockResponse(
        json_data={"error": "Invalid temperature value"},
        status_code=400
    )
    
    response = requests.post(f"{self.BASE_URL}/generate", json=payload)
    assert response.status_code == 400
    assert "error" in response.json()
```

## 👩‍💻 Author

**Mira Mamdoh Yousef Mossad**  
AI QA Engineer | ML Testing Specialist

- 📧 Email: miramamdoh10@gmail.com
- 💼 LinkedIn: [linkedin.com/in/mira-mamdoh-a9aa78224](https://www.linkedin.com/in/mira-mamdoh-a9aa78224)
- 🐙 GitHub: [github.com/miramamdoh23](https://github.com/miramamdoh23)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

Built as part of my journey into AI Quality Assurance, demonstrating professional testing methodologies for AI/ML applications. This framework showcases best practices in API testing, mock testing, and quality assurance for AI systems.

---

⭐ **If you find this project useful, please consider giving it a star!**

**Built with 💙 by Mira Mamdoh**