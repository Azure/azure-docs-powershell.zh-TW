---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794909"
---
# Get-AzsIPPool

## 摘要
傳回要求的 IP 池。

## 句法

###  (預設) 清單
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### 獲取
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## 說明
傳回要求的 IP 池。

## 示例

### 範例1： 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

取得所有基礎結構 ip 池。

### 範例2： 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

根據名稱取得基礎結構 ip 池。

## 參數

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -篩選
OData 篩選參數。

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -位置
資源的位置。

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -名稱
IP 池名稱。

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -PassThru
在命令成功時傳回 true

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId
可唯一識別 Microsoft Azure 訂閱的訂閱認證。
[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### IFabricAdminIdentity （FabricAdmin）的

## 輸出

### IIPPool （FabricAdmin）。 Api20160501。



## 筆記

複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。

INPUTOBJECT <IFabricAdminIdentity> ：身分識別參數
  - `[Drive <String>]`：儲存空間磁碟機的名稱。
  - `[EdgeGateway <String>]`： Edge 閘道的名稱。
  - `[EdgeGatewayPool <String>]`： Edge 閘道池的名稱。
  - `[FabricLocation <String>]`： Fabric 位置。
  - `[FileShare <String>]`： Fabric 檔案共用名稱。
  - `[IPPool <String>]`： IP 池名稱。
  - `[Id <String>]`：資源身分識別路徑
  - `[InfraRole <String>]`：結構角色名稱。
  - `[InfraRoleInstance <String>]`：結構角色實例的名稱。
  - `[Location <String>]`：資源的位置。
  - `[LogicalNetwork <String>]`：邏輯網路的名稱。
  - `[LogicalSubnet <String>]`：邏輯子網的名稱。
  - `[MacAddressPool <String>]`： MAC 位址集區的名稱。
  - `[Operation <String>]`： [操作識別碼]。
  - `[ResourceGroupName <String>]`：資源群組的名稱。
  - `[ScaleUnit <String>]`：縮放單位的名稱。
  - `[ScaleUnitNode <String>]`：縮放單位節點的名稱。
  - `[SlbMuxInstance <String>]`： SLB MUX 實例的名稱。
  - `[StoragePool <String>]`：儲存池名稱。
  - `[StorageSubSystem <String>]`：存儲系統的名稱。
  - `[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。 [訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。
  - `[Volume <String>]`：儲存空間量的名稱。

## 相關連結

