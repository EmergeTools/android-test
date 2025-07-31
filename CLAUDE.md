# Claude Code Project Configuration

This is a Bazel-based Android testing framework project.

## Build System
- **Primary Build Tool**: Bazel (using `bazelisk` command)
- **Language**: Java/Kotlin for Android
- **Project Type**: Android library/testing framework

## Key Commands
- **Build all**: `bazel build :axt_m2repository`
- **Build specific targets**: `bazel build //path/to/target`
- **Run tests**: `bazel test //path/to/test:target`

## Project Structure
- Uses Bazel BUILD files throughout the project
- Main repository build creates m2repository with all artifacts
- APKs are generated through the maven repository build process

## Important Build Targets
- `:axt_m2repository` - Builds the complete maven repository with all artifacts
- `//services:test_services` - Android Test Services APK
- `//runner/android_test_orchestrator/stubapp:stubapp` - Test Orchestrator APK

## Installation Script
- `build_and_install.sh` - Builds and installs orchestrator and services APKs locally