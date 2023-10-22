FROM golang:latest
WORKDIR /backend
COPY . .
RUN go mod download
RUN go build -o main .
EXPOSE 4000
CMD ["./main"]





# docker build -t go_react_todos/backend .
# docker run --rm -d -p 4000:4000 go_react_todos/backend
# docker run --rm -p 4000:4000 go_react_todos/backend
