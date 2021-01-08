FROM golang:1.8 AS build

WORKDIR /src
COPY . .
RUN go build -o /main .

FROM scratch

COPY --from=build /main /main
ENTRYPOINT ["/main"]