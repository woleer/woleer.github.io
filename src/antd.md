# antd 技巧

```javascript
  getPopupContainer={triggerNode => triggerNode.parentElement}
```

```javascript
const customRequest = (detail) => {
  console.log(detail);
  uploadPicture &&
    uploadPicture(detail.file).then((res) => {
      console.log(res.success);
    });
};

const headers = { "Content-Type": "multipart/form-data" };

<Upload
  accept="image/*"
  listType="picture-card"
  fileList={fileList}
  action={`${api.uploadPicture}`}
  multiple={true}
  customRequest={this.customRequest}
  withCredentials={true}
  beforeUpload={this.beforeUpload}
  onChange={handleFileListChange}
></Upload>;
```
