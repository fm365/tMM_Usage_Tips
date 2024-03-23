# tMM_Usage_Tips

## 电影重命名规则
`
${videoFormat}\${movie.country}\${title}.(${year}).${videoFormat}.${movie.mediaSource}${if movie.videoHDRFormat = "HDR10+"}.HDR2${else}${if movie.videoHDRFormat = "HDR10"}.HDR${else}${if movie.videoHDRFormat = "Dolby Vision"}.DV${else}${if movie.videoHDRFormat = "Dolby Vision, HDR10"}.DV${else}${if movie.videoHDRFormat = "Blu-ray HDR10"}.HDR${end}${end}${end}${end}${end}
`
