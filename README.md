

# Publish Docker Images  
Repository for publishing Docker images using GitHub Actions.

## Workflows

### 1. **DockerHub CI**  
This workflow builds and pushes Docker images to DockerHub.

- **Trigger:** Manually using `workflow_dispatch`.
- **Inputs:**  
  - `image_name`: Name of the Docker image (default: `hello-world`).
- **Secrets Required:**  
  - `DOCKERHUB_USERNAME`: Your DockerHub username.
  - `DOCKER_HUB_TOKEN`: DockerHub access token.

### 2. **GHCR CI**  
This workflow builds and pushes Docker images to GitHub Container Registry (GHCR).

- **Trigger:** Manually using `workflow_dispatch`.
- **Inputs:**  
  - `image_name`: Name of the Docker image (default: `hello-world`).
- **Secrets Required:**  
  - `GH_PAT`: GitHub Personal Access Token with `write:packages, delete:packages, read:packages, repo` permissions.

## Setup Instructions:
1. **Add Secrets:**
   - Go to your repository's **Settings > Secrets and variables > Actions**.
   - Add the necessary secrets (`DOCKERHUB_USERNAME`, `DOCKER_HUB_TOKEN`, `GH_PAT`).
   
2. **Trigger the Workflow:**
   - Go to the **Actions** tab.
   - Select the desired workflow (DockerHub CI or GHCR CI).
   - Click **Run workflow** and provide the `image_name` if needed.
