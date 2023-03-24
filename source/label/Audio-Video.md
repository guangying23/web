| 标签         | 描述                                                |
|--------------|-----------------------------------------------------|
| <a href="#audio">&lt;audio&gt;</a> New  | 定义声音，比如音乐或其他音频流。                    |
| <a href="#source">&lt;source&gt;</a> New | 定义media元素 (`<video>` 和`<audio>`)的媒体资源。media |
| <a href="#track">&lt;track&gt;</a> New  | 为媒体(`<video>` 和 `<audio>`)元素定义外部文本轨道。    |
| <a href="#video">&lt;video&gt;</a> New  | 定义一个音频或者视频                                |

1. <a id="audio">&lt;audio&gt;</a>

`<audio>` 标签定义声音，比如音乐或其他音频流。<br>
目前，`<audio>` 元素支持的3种文件格式：MP3、Wav、Ogg。<br>
| 浏览器            | MP3 | Wav | Ogg |
|-------------------|-----|-----|-----|
| Internet Explorer | YES | NO  | NO  |
| Chrome            | YES | YES | YES |
| Firefox           | YES | YES | YES |
| Safari            | YES | YES | NO  |
| Opera             | YES | YES | YES |

提示：可以在 `<audio>` 和 `</audio>` 之间放置文本内容，这些文本信息将会被显示在那些不支持 `<audio>` 标签的浏览器中。<br>
| 属性         | 值                 | 描述                                                        |
|--------------|--------------------|-------------------------------------------------------------|
| autoplay New | autoplay           | 如果出现该属性，则音频在就绪后马上播放。                    |
| controls New | controls           | 如果出现该属性，则向用户显示音频控件（比如播放/暂停按钮）。 |
| loop New     | loop               | 如果出现该属性，则每当音频结束时重新开始播放。              |
| muted New    | muted              | 如果出现该属性，则音频输出为静音。                          |
| preload New  | auto metadata none | 规定当网页加载时，音频是否默认被加载以及如何被加载。        |
| src New      | URL                | 规定音频文件的 URL。                                        |

`<audio>` 标签支持 HTML 的全局属性。<br>
`<audio>` 标签支持 HTML 的全局属性。<br>

2. <a id="source">&lt;source&gt;</a>

`<source>` 标签为媒体元素（比如 `<video>` 和 `<audio>`）定义媒体资源。<br>
`<source>` 标签允许您规定两个视频/音频文件供浏览器根据它对媒体类型或者编解码器的支持进行选择。<br>
| 属性      | 值          | 描述                                                                         |
|-----------|-------------|------------------------------------------------------------------------------|
| media New | media_query | 规定媒体资源的类型，供浏览器决定是否下载。                                   |
| src New   | URL         | 规定媒体文件的 URL。                                                         |
| type      | MIME_type   | 规定媒体资源的 MIME 类型。                                                   |
| sizes     |             | 不同页面布局设置不同图片大小。                                               |
| srcset    | URL         | `<source>` 应用于 `<picture>` 标签时需要使用到。指定在不同情况下使用的图像 URL。 |
  
`<source>` 标签支持 HTML 的全局属性。<br>
`<source>` 标签支持 HTML 的全局属性。<br>  

3. <a id="track">&lt;track&gt;</a>

`<track>` 标签为媒体元素（比如 `<audio>` and `<video>`）规定外部文本轨道，也就是字幕，字幕格式有 WebVTT 格式（.vtt 格式文件）。<br>
这个元素用于规定字幕文件或其他包含文本的文件，当媒体播放时，这些文件是可见的。<br>
| 属性        | 值                                                | 描述                                                                       |
|-------------|---------------------------------------------------|----------------------------------------------------------------------------|
| default New | default                                           | 规定该轨道是默认的。如果用户没有选择任何轨道，则使用默认轨道。             |
| kind New    | captions chapters descriptions metadata subtitles | 规定文本轨道的文本类型。                                                   |
| label New   | text                                              | 规定文本轨道的标签和标题。                                                 |
| src New     | URL                                               | 必需的。规定轨道文件的 URL。                                               |
| srclang New | language_code                                     | 规定轨道文本数据的语言。如果 kind 属性值是 "subtitles"，则该属性是必需的。 |

`<track>` 标签支持 HTML 的全局属性。<br>
`<track>` 标签支持 HTML 的全局属性。<br>  

4. <a id="video">&lt;video&gt;</a>

`<video>` 标签定义视频，比如电影片段或其他视频流。
目前，`<video>` 元素支持三种视频格式：MP4、WebM、Ogg。
| 浏览器            | MP4                                                     | WebM | Ogg |
|-------------------|---------------------------------------------------------|------|-----|
| Internet Explorer | YES                                                     | NO   | NO  |
| Chrome            | YES                                                     | YES  | YES |
| Firefox           | YES 从 Firefox 21 版本开始 Linux 系统从 Firefox 30 开始 | YES  | YES |
| Safari            | YES                                                     | NO   | NO  |
| Opera             | YES 从 Opera 25 版本开始                                | YES  | YES |

MP4 = MPEG 4文件使用 H264 视频编解码器和AAC音频编解码器
WebM = WebM 文件使用 VP8 视频编解码器和 Vorbis 音频编解码器
Ogg = Ogg 文件使用 Theora 视频编解码器和 Vorbis音频编解码器
提示：可以在 <video> 和 </video> 标签之间放置文本内容，这样不支持 <video> 元素的浏览器就可以显示出该标签的信息。
| 属性         | 值                 | 描述                                                                                        |
|--------------|--------------------|---------------------------------------------------------------------------------------------|
| autoplay New | autoplay           | 如果出现该属性，则视频在就绪后马上播放。                                                    |
| controls New | controls           | 如果出现该属性，则向用户显示控件，比如播放按钮。                                            |
| height New   | pixels             | 设置视频播放器的高度。                                                                      |
| loop New     | loop               | 如果出现该属性，则当媒介文件完成播放后再次开始播放。                                        |
| muted New    | muted              | 如果出现该属性，视频的音频输出为静音。                                                      |
| poster New   | URL                | 规定视频正在下载时显示的图像，直到用户点击播放按钮。                                        |
| preload New  | auto metadata none | 如果出现该属性，则视频在页面加载时进行加载，并预备播放。如果使用 "autoplay"，则忽略该属性。 |
| src New      | URL                | 要播放的视频的 URL。                                                                        |
| width New    | pixels             | 设置视频播放器的宽度。                                                                      |
  
`<video>` 标签支持 HTML 的全局属性。<br>
`<video>` 标签支持 HTML 的全局属性。<br>    
