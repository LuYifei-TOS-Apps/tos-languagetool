# LanguageTool on TOS privacy policy

This policy covers the self-hosted TOS package for LanguageTool. The NAS administrator operates the installation and controls its data and backups.

## Data and purpose

The HTTP API receives text and language options from the client and returns suggested corrections. The packaged server runs the checker locally on the NAS. The package does not mount a persistent text store. Container logs, proxies and clients may retain request metadata or other information depending on their logging settings.

## Sharing and external services

The bundled checker processes requests on the NAS. Connected clients and any proxy operated by the NAS administrator can read requests. Some clients may also offer a separate cloud service, depending on their settings.

Installation and updates can contact TOS distribution services and container registries to obtain packages and images. Requests to external services are handled according to the services and locations selected by the operator.

## Retention, access, correction and deletion

Clients can correct or replace text before submitting it again. Any copies in client history, proxy logs and Docker logs are subject to the relevant administrator's retention and deletion settings.

To remove an entire instance, stop it and identify the app-owned storage in Docker Manager before deleting it. The NAS administrator should handle retained backups separately and verify the effects of the TOS uninstall options. Contact the NAS administrator to request access, correction or deletion of data held by the instance.

## Security and support

The packaged port accepts unauthenticated HTTP requests. Restrict access to intended clients and use a TLS proxy before sending text across an untrusted connection.

For questions about the TOS package, use the repository's issue tracker. Omit private data, credentials and unredacted logs from public reports.
