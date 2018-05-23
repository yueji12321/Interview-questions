1.session 是存储服务器端，cookie 是存储在客户端，所以 session 的安全性比 cookie 高。</br>
2.获取 session 里的信息是通过存放在会话 cookie 里的 session id 获取的。而 session 是存放在服务器的内存中里，所以 session 里的数据不断增加会造成服务器的负担，所以会把很重要的信息存储在 session 中，而把一些次要东西存储在客户端的 cookie 里。</br>
3.cookie 确切的说分为两大类：会话 cookie 和持久化 cookie。会话 cookie 是存放在客户端浏览器的内存中，他的生命周期和浏览器是一致的，当浏览器关闭会话 cookie 也就消失了，而持久化 cookie 是存放在客户端硬盘中，持久化 cookie 的生命周期是我们在设置 cookie 时候设置的那个保存时间，session 的信息是通过 sessionid 获取的，而 sessionid 是存放在会话 cookie 当中的，当浏览器关闭的时候会话 cookie 消失，所以 sessionid 也就消失了，但是 session 的信息还存在服务器端，只是查不到所谓的 session 但它并不是不存在。所以 session 在服务器关闭的时候，或者是 sessio 过期，又或者调用了 invalidate()，再或者
是 session 中的某一条数据消失调用 session.removeAttribute() 方法，session 在通过调用 session.getsession 来创建的。
