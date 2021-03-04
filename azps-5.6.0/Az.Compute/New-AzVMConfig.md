---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1BECAC91-BB43-46EB-B2C9-C965C6FBC831
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMConfig.md
ms.openlocfilehash: 71aa555528ff1cdb5748c1a4ac62481ddd17c17c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912050"
---
# New-AzVMConfig

## 簡介
建立可配置的虛擬機器物件。

## 語法

### DefaultParameterSet (預設) 
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-Zone <String[]>] [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>]
 [-MaxPrice <Double>] [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD] 
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExplicitIdentityParameterSet
```
New-AzVMConfig [-VMName] <String> [-VMSize] <String> [[-AvailabilitySetId] <String>] [[-LicenseType] <String>]
 [-IdentityType] <ResourceIdentityType> [-IdentityId <String[]>] [-Zone <String[]>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-VmssId <String>] [-MaxPrice <Double>]
 [-EvictionPolicy <String>] [-Priority <String>] [-Tags <Hashtable>] [-EnableUltraSSD]
 [-EncryptionAtHost] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzMSConfig** Cmdlet 會為 Azure 建立可配置的本機虛擬機器物件。
其他 Cmdlet 可以用來設定虛擬機器物件，例如 Set-Az VIRTUALOperatingSystem、Set-Az VIRTUALSourceImage、Add-Az VIRTUALNetworkInterface 和 Set-Az VIRTUALOSSource。

## 例子

### 範例 1：建立虛擬機器物件
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
```

第一個命令會獲得名為 ResourceGroup11 的資源群組中名為 AvailabilitySet03 的可用性集，然後將該物件儲存在 $AvailabilitySet 變數中。
第二個命令會建立虛擬機器物件，然後將它儲存在$VirtualMachine變數中。
該命令會為虛擬機器指定名稱和大小。
虛擬機器屬於儲存在 $AvailabilitySet 的可用性集。

## 參數

### -AvailabilitySetId
指定可用性集的識別碼。
若要取得可用性集物件，請使用 Get-AzAvailabilitySet Cmdlet。
可用性集物件包含識別碼屬性。 <br>
相同可用性集指定的虛擬機器會配置給不同的節點，以最大化可用性。 <br>
有關可用性集的資訊，請參閱管理 [虛擬機器的可用性](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-manage-availability?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)。 <br>
有關 Azure 規劃維護的資訊，請參閱[Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-windows-planned-maintenance?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)虛擬機器的規劃維護 <br>
目前，VM 只能在建立時新增到可用性集。 要新增 VM 的可用性集應位於與可用性集資源相同的資源群組下。 現有的 VM 無法新增到可用性集。 <br>
此屬性無法與非 Null properties.virtualMachineScaleSet 參照一起存在。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### -EnableUltrasSD
啟用在 VM 上具有一或多個受管理的資料UltraSSD_LRS儲存空間帳戶類型。
只有啟用此屬性UltraSSD_LRS才能將具有儲存帳戶類型的受管理磁片新增到虛擬機器。


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Policy
Azure Spot 虛擬機器的回收政策。  支援的值為 'Deallocate' 和 'Delete'。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HostId
主機名稱

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityId
指定與虛擬機器縮放比例集相關聯的使用者身分設定清單。
使用者身分識別參照為表單中的 ARM 資源識別碼：'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identityies/{identityName}'

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IdentityType
虛擬機器的身分識別 ，如果已配置。

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
指定授權類型，表示虛擬機器的映射或磁片已授權于內部部署。
Windows Server 的可能值為：
- Windows_Client
- Windows_Server Linux Server 作業系統的可能值有： 
- RHEL_BYOS (RHEL)  
- SLES_BYOS (SUSE)  

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxPrice
指定您願意為低優先順序 VM/VMSS 支付的最高價格。 此價格為美元。 此價格會與 VM 大小目前低優先順序價格進行比較。 此外，在建立/更新低優先順序 VM/VMSS 時，會比較價格，且只有在 maxPrice 大於目前低優先順序價格時，作業才能成功。 如果建立 VM/VMSS 之後，目前的低優先順序價格超出 maxPrice，maxPrice 也會用於評估低優先順序的 VM/VMSS。 可能的值為：任何大於零的十進位值。 範例：0.01538。  -1 表示基於價格考慮，不應將低優先順序的 VM/VMSS 從上而退出。 此外，如果您未提供，預設最高價格為 -1。

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EncryptionAtHost
使用者可在要求中使用 EncryptionAtHost 屬性，以啟用或停用虛擬機器或虛擬機器縮放集的主機加密。 這會啟用所有磁片的加密，包括主機本身的資源/Temp 磁片。 預設：除非資源的此屬性設為 True，否則會停用主機的加密。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -優先順序
虛擬機器的優先順序。  只有支援的值是 "Regular"、'Spot' 和 'Low'。
"Regular" 適用于一般虛擬機器。
"Spot" 適用于 Spot 虛擬機器。
"Low" 也適用于 Spot 虛擬機器，但會由 "Spot" 取代。 請使用 "Spot" 而不是 "Low"。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProximityPlacementGroupId
要用於此虛擬機器的鄰近位置群組資源識別碼。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -標記
附加至資源的標記。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
指定虛擬機器的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
指定虛擬機器的大小。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmssId
虛擬機器縮放集的識別碼

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -區域
指定虛擬機器的可用性區域清單。 允許的值取決於區域的功能。 允許的值通常會是 1，2，3。

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

### System.String[]

### System.Collections.Hashtable

### System.Management.Automation.SwitchParameter

## 輸出

### Microsoft.Azure.Commands.Compute.models.PSVirtualMachine

## 筆記

## 相關連結

[Update-AzMS](./Update-AzVM.md)

[Set-AzEVOperatingSystem](./Set-AzVMOperatingSystem.md)

[Set-AzEVSourceImage](./Set-AzVMSourceImage.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)


