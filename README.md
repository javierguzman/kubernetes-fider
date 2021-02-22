# Kubernetes Fider Template Configuration

Do not forget to configure ingress setup with something like this under the rules section:

    - host: $WWW_FEEDBACK_HOST
      http:
        paths:
          - path: /
            backend:
              serviceName: feedback-server-service-$VERSION
              servicePort: 4003

    - host: $FEEDBACK_HOST
      http:
        paths:
          - path: /
            backend:
              serviceName: feedback-server-service-$VERSION
              servicePort: 4003
