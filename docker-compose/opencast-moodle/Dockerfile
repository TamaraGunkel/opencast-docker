FROM quay.io/opencast/allinone:9.2

COPY org.apache.karaf.features.cfg /opencast/etc/org.apache.karaf.features.cfg
COPY org.opencastproject.userdirectory.moodle-default.cfg /opencast/etc/org.opencastproject.userdirectory.moodle-default.cfg
COPY org.ops4j.pax.logging.cfg /opencast/etc/org.ops4j.pax.logging.cfg
COPY mh_default_org.xml /opencast/etc/security/mh_default_org.xml
COPY org.opencastproject.kernel.security.OAuthConsumerDetailsService.cfg /opencast/etc/org.opencastproject.kernel.security.OAuthConsumerDetailsService.cfg


COPY lms-automated-duplicate.xml /opencast/etc/workflows/lms-automated-duplicate.xml
COPY lms-publish-duplicate.xml /opencast/etc/workflows/lms-publish-duplicate.xml
COPY schedule-and-upload.xml /opencast/etc/workflows/schedule-and-upload.xml
COPY publish.xml /opencast/etc/workflows/publish.xml

EXPOSE 8090

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["app:start"]
