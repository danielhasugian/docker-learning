FROM alpine
ADD log-event.sh /
RUN chmod +x log-event.sh
RUN ["/log-event.sh", "image created"]
ENTRYPOINT ["/log-event.sh", "image runnings"]
