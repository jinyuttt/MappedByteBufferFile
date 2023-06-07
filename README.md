# MappedByteBufferFile
文件高速传输 内存映射方式读取存储文件

--------------------------------------------

 public static void main(String[] args) throws IOException, InterruptedException {

        long start=System.currentTimeMillis();
        FileChannelClient client = new FileChannelClient("127.0.0.1", 6606);
        client.connect();
        client.sendFile("E:\\soft\\vs2022.zip");
       System.out.println((System.currentTimeMillis()-start)/1000+"秒");
    }


  public static void main(String[] args) throws IOException {

        FileChannelServer ss = new FileChannelServer(6606);
        ss.Start();

    }
