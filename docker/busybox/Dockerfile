FROM microsoft/nanoserver

WORKDIR /busybox
ADD https://github.com/jhowardmsft/busybox64/raw/master/busybox.exe busybox.exe
RUN FOR /f "tokens=*" %i IN ('busybox --list') DO mklink C:\busybox\%i.exe busybox.exe
RUN setx /M PATH "C:\busybox;C:\;%PATH%"

WORKDIR %USERPROFILE%

ENTRYPOINT ["cmd.exe", "/s", "/c"]
