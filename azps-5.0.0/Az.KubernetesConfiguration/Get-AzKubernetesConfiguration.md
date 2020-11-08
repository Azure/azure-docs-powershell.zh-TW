---
external help file: ''
Module Name: Az.KubernetesConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.kubernetesconfiguration/get-azkubernetesconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KubernetesConfiguration/help/Get-AzKubernetesConfiguration.md
ms.openlocfilehash: 3fd93e42b8f38659f61fcbeb0f49040409f635a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140482"
---
# Get-AzKubernetesConfiguration

## 摘要
取得原始程式碼管理設定的詳細資料。

## 句法

###  (預設) 清單
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### 獲取
```
Get-AzKubernetesConfiguration -ClusterName <String> -ClusterRp <String> -ClusterType <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzKubernetesConfiguration -InputObject <IKubernetesConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## 說明
取得原始程式碼管理設定的詳細資料。

## 示例

### 範例1：取得 kubernetes 群集的所有設定
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

這個命令會取得 kubernetes 群集的所有設定。

### 範例2：依名稱取得 kubernetes 群集的設定
```powershell
PS C:\> Get-AzKubernetesConfiguration -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t02 -ClusterRp Microsoft.Kubernetes -ClusterType ConnectedClusters -Name conf-t02

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

這個命令會透過名稱取得 kubernetes 群集的設定。

### 範例3：依物件取得 kubernetes 群集的設定
```powershell
PS C:\> $kubConf = New-AzKubernetesConfiguration -Name conf-test02 -ClusterName connaks-dkc29c -ResourceGroupName connaks-rg-w9vlnp -RepositoryUrl http://github.com/xxxx
PS C:\> Get-AzKubernetesConfiguration -InputObject $kubConf

Name     Type
----     ----
conf-t02 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

這個命令會透過物件取得 kubernetes 群集的設定。

### 範例4：依管道取得 kubernetes 群集的設定
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/connaks-rg-w9vlnp/providers/Microsoft.Kubernetes/connectedClusters/connaks-d983yc/providers/Microsoft.KubernetesConfiguration/sourceControlConfigurations/conf-test01'} | Get-AzKubernetesConfiguration

Name        Type
----        ----
conf-test01 Microsoft.KubernetesConfiguration/sourceControlConfigurations
```

這個命令會透過管線取得 kubernetes 群集的設定。

## 參數

### -ClusterName
Kubernetes 群集的名稱。

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

### -ClusterRp
Kubernetes 群集 RP-AKS 群集的 ContainerService () 或 Microsoft. Kubernetes (OnPrem K8S 群集) 。

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

### -ClusterType
Kubernetes 群集資源名稱-AKS 群集的 managedClusters () 或 OnPrem K8S 群集) 的 connectedClusters (。

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

### -InputObject
要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.KubernetesConfiguration.Models.IKubernetesConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
來源控制項配置的名稱。

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SourceControlConfigurationName

Required: True
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Azure 訂閱 ID。
這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) 

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

### IKubernetesConfigurationIdentity （KubernetesConfiguration）的

## 輸出

### ISourceControlConfiguration （KubernetesConfiguration）。 Api20191101Preview。

## 筆記

別名

複雜的參數屬性

若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。 如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。


INPUTOBJECT <IKubernetesConfigurationIdentity> ：身分識別參數
  - `[ClusterName <String>]`： Kubernetes 群集的名稱。
  - `[ClusterResourceName <String>]`： Kubernetes 群集資源名稱-AKS 群集的 managedClusters () 或 OnPrem K8S 群集) 的 connectedClusters (。
  - `[ClusterRp <String>]`： Kubernetes 群集 RP-AKS 群集的 ContainerService () 或 Microsoft. Kubernetes (OnPrem K8S 群集) 。
  - `[Id <String>]`：資源身分識別路徑
  - `[ResourceGroupName <String>]`：資源群組的名稱。
  - `[SourceControlConfigurationName <String>]`：來源控制項配置的名稱。
  - `[SubscriptionId <String>]`： Azure 訂閱 ID。 這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) 

## 相關連結

