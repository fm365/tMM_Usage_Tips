# tMM_Usage_Tips

## 1.电影重命名规则
### 1.1 电影文件夹规则
`
${videoFormat}\${movie.country}\${title}.(${year}).${videoFormat}.${movie.mediaSource}${if movie.videoHDRFormat = "HDR10+"}.HDR2${else}${if movie.videoHDRFormat = "HDR10"}.HDR${else}${if movie.videoHDRFormat = "Dolby Vision"}.DV${else}${if movie.videoHDRFormat = "Dolby Vision, HDR10"}.DV.HDR${else}${if movie.videoHDRFormat = "Blu-ray HDR10"}.HDR${end}${end}${end}${end}${end}
`
### 1.2 电影文件规则
`
${if movie.originalTitle = movie.title}${movie.title}${else}${movie.title}.${movie.originalTitle}${end}.${year}.${movie.mediaSource}${if movie.note = 'REMUX'}.REMUX${end}.${movie.mediaInfoVideoFormat}.${movie.mediaInfoVideoCodec}.${videoBitDepth}bit.${audioCodec}.${audioChannels}${if movie.videoHDRFormat = "HDR10+"}.HDR2${else}${if movie.videoHDRFormat = "HDR10"}.HDR${else}${if movie.videoHDRFormat = "Dolby Vision"}.DV${else}${if movie.videoHDRFormat = "Dolby Vision, HDR10"}.DV.HDR${else}${if movie.videoHDRFormat = "Blu-ray HDR10"}.HDR${end}${end}${end}${end}${end}.${edition}
`

## 2.电视重命名规则
### 2.1 电视文件夹规则
`
${showTitle}.(${showYear})
`
### 2.2 季文件夹规则
`
Season.${seasonNr2}.${seasonName}${if episode.note = 'REMUX'}.REMUX${end}.${videoFormat}${if episode.videoHDRFormat = "HDR10+"}.HDR2${else}${if episode.videoHDRFormat = "HDR10"}.HDR${else}${if episode.videoHDRFormat = "Dolby Vision"}.DV${else}${if episode.videoHDRFormat = "Blu-ray HDR10"}.HDR${else}${if episode.videoHDRFormat = "HDR"}.HDR${else}${if episode.videoHDRFormat = "Dolby Vision, HDR10"}.DV.HDR${end}${end}${end}${end}${end}${end}
`
### 2.2 电视文件规则
`
${tvShow.title}.${if tvShow.title=season.title}S${seasonNr2}E${episodeNr2}${else}S${seasonNr2}.${seasonName}.S${seasonNr2}E${episodeNr2}${end}.${title}.${mediaSource}${if episode.note = 'REMUX'}.REMUX${end}.${videoFormat}.${videoCodec}.${videoBitDepth}bit.${audioCodec}${if episode.videoHDRFormat = "HDR10+"}.HDR2${else}${if episode.videoHDRFormat = "HDR10"}.HDR${else}${if episode.videoHDRFormat = "Dolby Vision"}.DV${else}${if episode.videoHDRFormat = "Blu-ray HDR10"}.HDR${else}${if episode.videoHDRFormat = "HDR"}.HDR${else}${if episode.videoHDRFormat = "Dolby Vision, HDR10"}.DV.HDR${end}${end}${end}${end}${end}${end}
`
