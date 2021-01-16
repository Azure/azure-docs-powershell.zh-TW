---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdMsixPackage.md
ms.openlocfilehash: 559cff58ac8d6c3f3d8f116b6147d6f4c2a4378d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275544"
---
# Get-AzWvdMsixPackage

## 摘要
取得 msixpackage。

## 句法

###  (預設) 清單
```
Get-AzWvdMsixPackage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 獲取
```
Get-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 說明
取得 msixpackage。

## 示例

### 範例1：依名稱取得 MSIX 套件
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName                     Microsoft.DesktopVirtualization/hostpools/msixpackages
```

這個命令會在 HostPool 中取得 MSIX 套件。

### 範例2：清單 MSIX 套件 
```powershell
PS C:\> Get-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId

Name                                                  Type
----                                                  ----
HostPoolName/MSIXPackage_FullName1                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName2                    Microsoft.DesktopVirtualization/hostpools/msixpackages
HostPoolName/MSIXPackage_FullName3                    Microsoft.DesktopVirtualization/hostpools/msixpackages
```

這個命令會列出 HostPool 中的 MSIX 套件。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -FullName
指定 hostpool 中 MSIX 套件的版本特定套件完整名稱

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostPoolName
指定資源群組中主機池的名稱

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。
名稱不區分大小寫。

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
目標訂閱的 ID。

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

### IDesktopVirtualizationIdentity （DesktopVirtualization）的

## 輸出

### IMsixPackage （DesktopVirtualization）。 Api20201019Preview。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數
  - `[ApplicationGroupName <String>]`：應用程式群組的名稱
  - `[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱
  - `[DesktopName <String>]`：指定的桌面群組中的桌面名稱
  - `[HostPoolName <String>]`：指定資源群組中的主機池名稱
  - `[Id <String>]`：資源身分識別路徑
  - `[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱
  - `[ResourceGroupName <String>]`：資源群組的名稱。 名稱不區分大小寫。
  - `[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱
  - `[SubscriptionId <String>]`：目標訂閱的識別碼。
  - `[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱
  - `[WorkspaceName <String>]`：工作區的名稱

## 相關連結

