
# `curl` Command Examples

`curl` is a versatile command-line tool used for transferring data with URLs. It supports various protocols, including HTTP, HTTPS, FTP, and more. Below are some common usages of `curl` commands.

## 1. Basic `GET` Request

Fetch the content of a webpage:

```bash
curl https://www.example.com/
```

This command retrieves the HTML content of the specified URL.

## 2. Save Output to a File

Download a file and save it with a specific name:

```bash
curl -o filename.html https://www.example.com/
```

The `-o` option saves the fetched content to `filename.html`.

To save the file with its original name from the URL:

```bash
curl -O https://www.example.com/index.html
```

The `-O` option uses the remote file's name and saves it in the current directory.

## 3. Follow Redirects

Some URLs may redirect to another location. To allow `curl` to follow redirects:

```bash
curl -L https://www.example.com/
```

The `-L` option instructs `curl` to follow any redirects until the final destination is reached.

## 4. Perform a `POST` Request

Send data to a server using a `POST` request:

```bash
curl -X POST -d "param1=value1&param2=value2" https://www.example.com/api
```

This command sends form-encoded data to the specified URL.

To send JSON data:

```bash
curl -X POST -H "Content-Type: application/json" -d '{"key1":"value1","key2":"value2"}' https://www.example.com/api
```

Here, the `-H` option sets the `Content-Type` header to `application/json`, and the `-d` option sends the JSON data.

## 5. Include Headers in the Output

To include HTTP headers in the output:

```bash
curl -i https://www.example.com/
```

The `-i` option includes the HTTP response headers in the output.

## 6. Set Custom Request Headers

Add custom headers to the request:

```bash
curl -H "Authorization: Bearer YOUR_TOKEN" https://www.example.com/api
```

This command adds an `Authorization` header with a bearer token to the request.

## 7. Upload a File

Upload a file to a server:

```bash
curl -F "file=@/path/to/your/file.txt" https://www.example.com/upload
```

The `-F` option specifies form data, and the `@` symbol indicates the file to be uploaded.

## 8. Download Multiple Files

Download multiple files in a single command:

```bash
curl -O https://www.example.com/file1.txt -O https://www.example.com/file2.txt
```

This command downloads `file1.txt` and `file2.txt` from the specified URL.

## 9. Resume a Download

Resume an interrupted download:

```bash
curl -C - -O https://www.example.com/largefile.zip
```

The `-C -` option tells `curl` to continue the download from where it left off.

## 10. Use a Proxy

Route the request through a proxy server:

```bash
curl -x http://proxyserver:port https://www.example.com/
```

The `-x` option specifies the proxy server and port to use for the request.

---

For more detailed information and options, refer to the [cURL Manual](https://curl.se/docs/manual.html).
