# https://github.com/baosystems/docker-postgis/pkgs/container/postgis
# FROM ghcr.io/baosystems/postgis:15-3.3 - 2023.08.29
FROM ghcr.io/baosystems/postgis:15-3.4

# 시간을 서울로 변경 처리 & ko_KT.UTF-8 로케일 생성
ENV TZ=Asia/Seoul
RUN ln -sf /usr/share/zoneinfo/$TZ /etc/localtime && \
    sed -i 's/# ko_KR.UTF-8 UTF-8/ko_KR.UTF-8 UTF-8/' /etc/locale.gen && \
    locale-gen

# 환경변수 설정
ENV LANG=ko_KR.UTF-8 \
		LANGUAGE=ko_KR.UTF-8 \
    LC_ALL=ko_KR.UTF-8 \
    POSTGRES_INITDB_ARGS=--data-checksums