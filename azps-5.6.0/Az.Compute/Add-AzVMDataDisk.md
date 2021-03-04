---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 685a1768dac652b3981bd081a2f8b29997c08639
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909213"
---
# Add-AzVMDataDisk

## 簡介
新增資料磁片至虛擬機器。

## 語法

### VmNormalParameterSetName (預設) 
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### VmManagedParameterSetName
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Add-AzCMDataDataData Cmdlet** 會將資料磁片新增到虛擬機器。
您可以在建立虛擬機器時新增資料磁片，也可以新增資料磁片至現有的虛擬機器。

## 例子

### 範例 1：新增資料磁片至新的虛擬機器
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

第一個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。
該命令會為虛擬機器指定名稱和大小。
接下來三個命令會指派三個數據磁片的路徑給$DataDiskVhdUri 01、$DataDiskVhdUri 02 和 $DataDiskVhdUri 03 變數。
此方法僅適用于下列命令的可讀性。
最後三個命令各自會將資料磁片新增到儲存在 $VirtualMachine 中的虛擬機器。
命令會指定磁片的名稱和位置，以及磁片的其他屬性。
每個磁片的 URI 會儲存在 $DataDiskVhdUri 01、$DataDiskVhdUri 02 和 $DataDiskVhdUri 03。

### 範例 2：新增資料磁片至現有的虛擬機器
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

第一個命令會使用 [Get-Az VIRTUAL](./Get-AzVM.md) Cmdlet 取得名為 VirtualMachine07 的虛擬機器。
該命令將虛擬機器儲存在 $VirtualMachine 變數中。
第二個命令會將資料磁片新增到儲存在 $VirtualMachine 的虛擬機器。
最後一個命令會更新儲存在 ResourceGroup11 $VirtualMachine的狀態。

### 範例 3：從一般使用者映射新增資料磁片至新虛擬機器
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

第一個命令會建立虛擬機器物件，並儲存在$VirtualMachine變數中。
該命令會為虛擬機器指定名稱和大小。
接下來兩個命令會分別將資料影像和資料磁片路徑指派給$DataImageUri$DataDiskUri變數。
此方法用來改善下列命令的可讀性。
最後的命令會將資料磁片新增到儲存在 $VirtualMachine 中的虛擬機器。
命令會指定磁片的名稱與位置，以及磁片的其他屬性。

### 範例 4：從特殊使用者映射新增資料磁片至新虛擬機器
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

第一個命令會建立虛擬機器物件，並儲存在$VirtualMachine變數中。
該命令會為虛擬機器指定名稱和大小。
下一個命令會指定資料磁片的路徑至$DataDiskUri變數。
此方法用來改善下列命令的可讀性。
最後一個命令是新增資料磁片至儲存在 $VirtualMachine。
命令會指定磁片的名稱和位置，以及磁片的其他屬性。

## 參數

### -緩存
指定磁片的緩存模式。
此參數可接受的值為：
- ReadOnly
- 朗讀
- None 預設值為 ReadWrite。
變更此值會導致虛擬機器重新開機。
此設定會影響磁片的一致性與績效。

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
指定此 Cmdlet 是否要從平臺或使用者映射在虛擬機器中建立磁片、建立空白磁片，或附加到現有的磁片。
此參數可接受的值為：
- 附加。
指定此選項以從特殊磁片建立虛擬機器。
當您指定此選項時，請勿指定 *SourceImageUri* 參數。
*VhdUri* 是告知 Azure 平臺虛擬硬碟 (VHD) 以資料磁片附加至虛擬機器所需的一切。
- 空。
指定此選項以建立空白的資料磁片。
- FromImage.
指定此選項以從一般圖像或磁片建立虛擬機器。
當您指定此選項時，您必須指定 *SourceImageUri* 參數，才能告訴 Azure 平臺要附加為數據磁片的 VHD 位置。
*VhdUri* 參數會用來當虛擬機器使用資料磁片 VHD 時，用來識別資料磁片 VHD 儲存的位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId
指定客戶管理的磁片加密集的資源識別碼。  這僅適用于受管理的磁片。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
指定要附加到虛擬機器的空白磁片大小 ，以 GB 為單位。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -四分位
指定資料磁片的 (或) 邏輯單位編號。

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Managed也Id
指定受管理磁片的識別碼。

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要新增的資料磁片名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SourceImageUri
指定此 Cmdlet 所附加到磁片的來源 URI。

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
指定受管理磁片的儲存帳戶類型。

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
指定虛擬硬碟 (VHD) 檔案的統一資源識別項 (URI) ，以在使用平臺映射或使用者映射時建立。
此 Cmdlet 會複製圖像二進位大型物件 (blob) 到此位置。
這是啟動虛擬機器的位置。

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
指定要新增資料磁片的本機虛擬機器物件。
您可以使用 **Get-AzMS** Cmdlet 來取得虛擬機器物件。
您可以使用 **New-AzMSConfig** Cmdlet 來建立虛擬機器物件。

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

### System.String

### Microsoft.Azure.management.Compute.models.CachingTypes

### System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

### Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT

## 筆記

## 相關連結

[Remove-AzDATAData一體式應用程式](./Remove-AzVMDataDisk.md)

[Get-AzMS](./Get-AzVM.md)

[New-AzMSCONFIG](./New-AzVMConfig.md)
