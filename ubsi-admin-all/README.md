# Cloud Native Architecture Overview

Cloud native architecture is currently the mainstream method for building modern application systems. It emphasizes building and running applications in the cloud environment and has the following basic characteristics: componentization, observability, independently deployable/testing, dynamically upgradable/replaceable, and configurable management, among others. Cloud native is a set of technologies and methodologies, primarily consisting of microservices, DevOps, continuous delivery, and containerization.

## Unified Basic Service Infrastructure (UBSI)

UBSI is a lightweight microservices architecture platform designed to provide a fast, simple, and easy-to-use microservices development and governance solution. Compared to SpringCloud, UBSI also builds a complete microservices development/governance system, aiming to simplify the microservices development process and improve development efficiency and system maintainability.

## Quick Start

1. **Domain Access Configuration**:

   - Ensure that your domain name server or local hosts can resolve `rewin.ubsi.admin.com`.

2. **Install Extension Components**:

   - After installation, click the `ubsi-admin` button in the upper left corner of the KubeSphere platform to enter the UBSI-admin console.
   - It may take a few minutes to load the components for the first time.

3. **Initial Account Setup**:

   - Super administrator account: `admin`
   - Initial password: `abcde321`

4. **Use document**: 

   - Before embarking on the exploration journey of UBSI, it is worth taking some time to thoroughly read its official development documentation, which will lay a solid foundation for your future development work. The document can be obtained through the following link: [UBSI Development Document](https://ubsi-home.github.io/docs/index.html). 

## Advanced Configuration

1. **Extension Component Configuration Adjustment**:

   - In the "Extension Component Configuration" interface, adjust the `architecture` and `replicaCount` fields for the `redis` and `mongodb` groups according to production needs.
     - The `architecture` defaults to `standalone` (single node), suitable for development environments.
     - The `replicaCount` defaults to 1 and can be adjusted based on enterprise-level requirements.

2. **Storage Component Configuration**:

   - In UBSI, you need corresponding storage (MongoDB, Redis, Nexus, etc.).
   - Before installation, configure the Kubernetes StorageClass to ensure support for the automatic creation of PVC (Persistent Volume Claim), achieving data persistence.

3. **Post-Installation Operations**:

   - After all Pods are installed, restart the `ubsi-admin-container` and `ubsi-webapi` containers to ensure that the latest configuration takes effect.
   - You can then start development work.

## Obtaining a License

1. **Version Description**:

   - UBSI-admin is divided into enterprise and development versions.
   - The development version does not require a license and can be used for free in development/testing environments.
   - A license is required for deploying in a production environment, and you need to apply for a license to upgrade the development version to the enterprise version.

2. **Steps to Obtain a License**:

   - Click "Subscribe," select the corresponding version, and purchase the extension components.
   - After the purchase is successful, send the IP address of the deployed redis and mongodb svc to the email: `ubsi@rewin.com.cn`.
   - After receiving the license file, modify the content into a configuration dictionary named `ubsi-admin-license`.
   - After modifying the configuration dictionary of 'ubsi admin license', it is necessary to restart the 'ubsi admin container' container to ensure that the latest configuration takes effect.

## Business Consultation

For more information, please visit the company's website: [UBSI Microservices Architecture Platform Homepage](https://ubsi-home.github.io/), or contact us for business consultation via email: `ubsi@rewin.com.cn`.

We hope this installation guide will help you deploy the UBSI platform smoothly. If you have any questions, please feel free to contact us for support.