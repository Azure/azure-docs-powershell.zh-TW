---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRMVhd.md
ms.openlocfilehash: 7faa179ae8c8c43d750e4f042f7bc925b772f4e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448770"
---
# Add-AzureRmVhd

## 摘要
將虛擬硬碟從內部部署虛擬機器上傳到 Azure 中雲端儲存空間帳戶的 blob。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Add-AzureRmVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [<CommonParameters>]
```

## 說明
**AzureRmVhd** Cmdlet 會將內部部署虛擬硬碟（.vhd 檔案格式）上傳到 blob 儲存空間帳戶做為固定虛擬硬碟。
您可以設定將在指定的目標 URI 中使用或覆寫現有 blob 的上載程式執行緒數。
此外，也支援上傳已修正版本的內部部署 .vhd 檔案的功能。
當基本虛擬硬碟已上傳時，您可以上傳使用基本映射作為父級的差異磁片。
還支援共用存取簽名 (SAS) URI。

## 示例

### 範例1：新增 VHD 檔案
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

這個命令會將 .vhd 檔案新增至儲存空間帳戶。

### 範例2：新增 VHD 檔案並覆寫目的地
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

這個命令會將 .vhd 檔案新增至儲存空間帳戶。
此命令會覆寫現有的檔案。

### 範例3：新增 VHD 檔案並指定執行緒數
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

這個命令會將 .vhd 檔案新增至儲存空間帳戶。
命令會指定要用來上傳檔案的執行緒數。

### 範例4：新增 VHD 檔案並指定 SAS URI
```
PS C:\> Add-AzureRmVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

這個命令會將 .vhd 檔案新增至儲存空間帳戶，並指定 SAS URI。

## 參數

### -BaseImageUriToPatch
指定 Azure Blob 儲存空間中基本映射 blob 的 URI。
您可以將 SAS 指定為此參數的值。

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -目的地
指定 Blob 儲存區中的 blob URI。
雖然修補案例目的地不能是 SAS URI，但參數支援 SAS URI。

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalFilePath
指定本機 .vhd 檔案的路徑。

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberOfUploaderThreads
指定上傳 .vhd 檔案時要使用的上載程式執行緒數。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OverWrite
指示這個 Cmdlet 會覆寫指定的目標 URI （如果有的話）中現有的 blob （如果有的話）。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定虛擬機器之資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

## 筆記

## 相關連結

[儲存-AzureRmVhd](./Save-AzureRmVhd.md)


