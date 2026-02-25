# 二维码生成器项目规则

## 项目说明

订阅链接二维码生成器，支持 Clash / Surge / Shadowrocket / Quantumult 订阅链接。

## 技术栈

- 纯 HTML/CSS/JavaScript，无框架
- 二维码库：`qrcode-generator` (支持超长内容)
- CDN：bootcdn

## 开发流程（必须遵守）

### 完整测试流程

当修改代码后，**必须**使用 Chrome DevTools MCP 进行完整测试：

```
代码修改 → Chrome DevTools 测试 → 验证通过 → 任务完成
```

### 测试步骤

1. **打开/刷新页面**
   ```
   new_page(url) 或 press_key("Control+Shift+R") 强制刷新
   ```

2. **填入测试数据**
   ```
   fill(uid, value) - 填入输入框
   ```

3. **触发操作**
   ```
   click(uid) - 点击按钮
   ```

4. **检查结果**
   ```
   take_snapshot() - 检查页面结构
   take_screenshot() - 截图确认视觉效果
   ```

5. **检查控制台**
   ```
   list_console_messages(types=["error", "warn"]) - 确认无错误
   ```

6. **测试所有相关功能**
   - 复制功能
   - 下载功能
   - 清空功能
   - 粘贴功能

### 测试标准

- ✅ 无控制台错误
- ✅ 页面正常渲染
- ✅ 所有按钮功能正常
- ✅ Toast 提示正确显示

只有全部通过才算任务完成。

## 测试用例

### 长链接测试

使用以下超长链接测试二维码生成：

```
vless://ec005dda-dc96-4aff-a8ca-a37fa21632ef@cf.hellohub.top:443?type=tcp&encryption=none&security=reality&pbk=NOz1f3QuKnIcjrY3EC4gs2nDJcRS8cR7Qar5GoxI-Dc&fp=chrome&sni=tesla.com&sid=7acd8f51116e7e&spx=%2F&pqv=hHlUhBUK0syQsg6u6p_YIZ2MwcphbRi97azIUA1-mxYhrlM_4VRnO5aYvzy_Nvp4JCTnwElO4UknZ5m1D27HL6RfBRzJSEzKM9RXS91SqiDvK3DIiyZZoW9QNYoiBO9KxB886BABLPTlyjskEXfZ_xDEvO1Z0m4GOWe7idGRw9FrsD6sTM8k9CF-T1FVMvqfA4k6ijc31I2f_k-pcaVXo2tQGT7jkjAJKiHHTOHifiTOPB2jEEV2Epr476wSpRdTa2W-Qmha1wFvLh3n71FylvKyOhUZYFI0taY96QkuLwpBSEOtwocLHtQNOcVwSzRcAWQbmWGf68vqrycaVEFMeOFxJBY4BhROxd8iDMgGIwJW8PlgidYDQdx4jMFOTQtU2_IIFQHwPQw7RgwztXAfzFzW4CA-py4bDsc6gljYPuoYvXF0XsocLMTgJD9N8wkrV8jcQe4Vb9etKSXGjUoSWTL_aIkmb8o-rjCy7XVO2iogaJMe0nOFbMwqHXA1CMmO495YaE2v-gJKABHiFOyXK8Xxzgbo-i6pfnrUKt4DusjEjveGtOMRGRQ0uDOn3nRucHmLT8b2xH5fYJeI_bQEQEAEX0ui4wqpTI4tPofE22BVToEQV7lQ-H0pDSCrYxDZ9HkC4YqTI4S27hKGhye1oobHdwgEhFACdGzayYEE6LHfYFqf_VokQIoGpY9vXXYXKdvO2RK1KaBV6o4ZwbqFHDcVSIMB_g5i8UbptOQrWHnvW78kt4x4hMsi9iz0XRjJyLjfuUQok8BhOPV616MYCJEGOsxR8un42UW1fDWs2bL6_AHm4nRnkMi3d4dHOTVScIAOXM9_tKoTxLoQow6qqK4AIjWEd9xFBKCWfZq0PzFm_lzihunl0nxfi912_IUIpkjv0_2_LAeNOhhbrgweHCg0UkwZgeoYm4GjUoIQNwgu-OyBqMe-GOJILONRZCbDJmSTQ4aaQLflwM07oV_0agsg1_VJv2H_WGickSVP07U5EtLqsVcwBOT3BUPgG4tMUVGsXuvDeo1t5czIbLBNZerMyIW8BN2__N6cCzj7i2ivogIE2TcaVKeafQ26QxRBSzj4KUn7kwzbI2jfK_y-oeJ5Kv7pxd0UMURmRrz5zJj1WLSOmUK79RAhvOv6TADVkSMUFPOLnzmq74H6NON9eo9WyhYAnxSuRjfILCT_10PdSwiPnwttr_oIg-aMf40pa6-esgoocFtwOEOv34UYdqxwP-fdf4qRftZbUiTAjj03oCu6BFXdrLCpO9KngNrbRcHny4gzbbVHhu1EljY198BS3txvXyQ-Bc46FTojuB3D275Mqtqcwkti0p3ASQmpsuC7NtTTKl3DM1NoM_AZ0NGAvGp8_sVjfghXFy_p3QO4rZ6e47DHhv7eBj6LjnOgb-A6nkAlBYfUNqJV-xLbf72TBpWBcTB6wNvE9hEb8xqg7PpldrI9m3S5vWKge-2sB7zUZHvktZZF-wA3QXhdpNU1RoH6sO-povAPygw-AdeuWKG4UM28TcAecywWH5OTZjxRs17qKEQMu9kdtZC_fYoX8lyv1AUwUmIpPY2grNt8UzBE72hEZ4ln8kActFTvMVTN3jX9bB7bhbDZFykKQMTJfPtF3jMekyErRJGQFrHhuugKVvXs5clAmwq1IHr-awWO-Nt3VCtDnknsPvPQaQsDpNF0gHX2a0fRPeyvmlUL0gyCvRnPi9UUoB7CXxLOqjridjdJ7s9SIel53_aOcyYyoqu6xh3IByJI6-XrfdQrVx0RA7zhjnyhaPi8oPh8dN4CvXlo0B_SI4caLqncFr2YUBTU8yXL1HkrSS_wSOTtsDOecpb7GhaHES__nn0kcihfg2WQ201CnmBvrGZnXhNdJ8G0rraPUg9DHoNRWEKyVR8muQrL1ZePuUdLW3gpva0l2h11rbrYfmNhiK0vlOIZaZzB19QjnkAgPafgjr8FbcbYS70LzM-gdwqBXUttFafJzEaNkv5iN1ngPO20wBT8UGBilHyU6QIllz2fOQYDQrNa-S4jiQHOUHAr_rEye_2JZdZnfXh7A9aAtiydNApJlcbOrZYI_T9m3-DscY2rkKXcpvZDNFitMgL8PrkSkQ_qjUwe7DV3F0xOe5qOcn5rl3YKgGDYRBM5D-OreUn1q7PowH8HvJMDdZrc0IwRQ1oqKjerdMDhbpf0-a9Sl2BsXTmmqOUNxFQE_r7quZF1074PNo956Gh-DFfWapRzyXLj-ZplazVmbEcCXj9QKWMSDK9FLEtIflGl9RflzgFjsKtNqTKVAyM2F77_ThnD8w75_cciC-av6ffc-2WpS3JRvh31-943w0_PKqyrJq5qw2zXOt_8esvOW3F-MZRSFtCFy9-SsUG0mjXCjT5Tw-TlziHKIKPNPoVRxKZ92nptYaQt0ATjC-Zkb1vsDjd_71iEe-ZkrTG7EDE4KD5Ff5M4VBmuM7_YLOmk_V-zm119ISyZ6rvm2TpP9SGckr-bKeIskvHAilTbkmDXPltbb03PKk0u88ImfOJomB_zin_7JEvj1_sMSRna4m8Nb3gouUx_cunwExIKFv9mBj0cNzQ7JP_8KDoKu3NfYgvmigo#4zsv8mx4
```

### 多链接测试

每行一个链接，测试批量生成功能。

## 注意事项

- 二维码库使用 `qrcode-generator`，不是 `qrcodejs` 或 `qrcode`
- 纠错级别使用 `L`（低），以容纳更多数据
- CDN 使用 bootcdn，避免 `file://` 协议下的跨域问题
