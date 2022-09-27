# dcompose
실행 시 주의사항
=============
./backend_build 경로에 repository 디렉터리가 있어야 합니다.
해당 디렉터리는 maven repository에서 받아온 jar 파일들이 들어있으며
리눅스 기준 /root/.m2/repository 와 같다고 보시면 됩니다.

이 디렉터리가 존재하는 이유는 maven 빌드 시 의존 파일을 다운로드 하는 시간을 아끼기 위해서 입니다.
다음 링크에 존재하는 파일을 ./backend_build 디렉터리에서 압축 해제 하시면 됩니다.

https://drive.google.com/file/d/17wbwY_Dz0rBwu-wBLJo-XKM3C85fYxWk/view?usp=sharing

만약 해당 파일을 이용하고 싶지 않으시다면 ./backend_build/Dockerfile 에서
2번째 줄, COPY ..... 를 주석처리 하시면 됩니다.
