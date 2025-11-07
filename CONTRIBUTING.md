# Contributing to College Cosmos Home

Thank you for your interest in contributing to College Cosmos Home! We welcome contributions from everyone.

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Git
- A GitHub account

### Setting Up Your Development Environment

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/yourusername/college-cosmos-home.git
   cd college-cosmos-home
   ```
3. **Add the upstream remote**:
   ```bash
   git remote add upstream https://github.com/originalowner/college-cosmos-home.git
   ```
4. **Install dependencies**:
   ```bash
   npm install
   ```
5. **Create a branch** for your feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## 📝 How to Contribute

### Reporting Bugs
- Use the GitHub issue tracker
- Check if the issue already exists
- Provide detailed reproduction steps
- Include system information and screenshots

### Suggesting Features
- Open an issue with the "enhancement" label
- Describe the feature and its benefits
- Discuss implementation approaches

### Code Contributions

#### Pull Request Process
1. **Update your fork** with the latest changes:
   ```bash
   git fetch upstream
   git checkout main
   git merge upstream/main
   ```

2. **Create a feature branch**:
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Make your changes** following our coding standards

4. **Test your changes**:
   ```bash
   npm run test
   npm run lint
   ```

5. **Commit your changes**:
   ```bash
   git commit -m "feat: add amazing feature"
   ```

6. **Push to your fork**:
   ```bash
   git push origin feature/amazing-feature
   ```

7. **Create a Pull Request** on GitHub

## 📋 Coding Standards

### JavaScript/React Guidelines
- Use ES6+ features
- Follow React best practices
- Use functional components with hooks
- Implement proper error handling
- Write meaningful variable and function names

### Code Style
- Use Prettier for formatting
- Follow ESLint rules
- Use 2 spaces for indentation
- Use semicolons
- Use single quotes for strings

### Commit Messages
Follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

- `feat:` - New features
- `fix:` - Bug fixes
- `docs:` - Documentation changes
- `style:` - Code style changes
- `refactor:` - Code refactoring
- `test:` - Adding or updating tests
- `chore:` - Maintenance tasks

Examples:
```
feat: add real-time bus tracking
fix: resolve authentication issue
docs: update API documentation
```

## 🧪 Testing

- Write unit tests for new features
- Ensure all tests pass before submitting PR
- Include integration tests where appropriate
- Test on multiple browsers and devices

### Running Tests
```bash
npm run test          # Run all tests
npm run test:watch    # Run tests in watch mode
npm run test:coverage # Generate coverage report
```

## 📚 Documentation

- Update README.md if needed
- Add JSDoc comments for functions
- Update API documentation
- Include examples for new features

## 🔍 Code Review Process

1. **Automated checks** must pass (CI/CD)
2. **Code review** by maintainers
3. **Testing** in development environment
4. **Approval** and merge

### Review Criteria
- Code quality and readability
- Performance implications
- Security considerations
- Test coverage
- Documentation completeness

## 🏷️ Issue Labels

- `bug` - Something isn't working
- `enhancement` - New feature request
- `documentation` - Documentation improvements
- `good first issue` - Good for newcomers
- `help wanted` - Extra attention needed
- `priority: high` - High priority issues

## 💬 Communication

- **GitHub Issues** - Bug reports and feature requests
- **Discussions** - General questions and ideas
- **Discord** - Real-time chat with the community

## 📜 Code of Conduct

### Our Pledge
We pledge to make participation in our project a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, gender identity and expression, level of experience, nationality, personal appearance, race, religion, or sexual identity and orientation.

### Expected Behavior
- Be respectful and inclusive
- Exercise empathy and kindness
- Focus on what's best for the community
- Accept constructive criticism gracefully

### Unacceptable Behavior
- Harassment or discriminatory language
- Personal attacks or trolling
- Public or private harassment
- Publishing others' private information

## 🎉 Recognition

Contributors will be recognized in:
- README.md contributors section
- Release notes for significant contributions
- Special mentions in project updates

## ❓ Questions?

Don't hesitate to ask questions! You can:
- Open an issue with the "question" label
- Join our Discord community
- Email us at contributors@collegecosmos.com

Thank you for contributing to College Cosmos Home! 🚌✨