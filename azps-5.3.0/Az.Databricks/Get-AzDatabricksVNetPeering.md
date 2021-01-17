---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436631"
---
# <span data-ttu-id="b55bc-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="b55bc-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="b55bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b55bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b55bc-103">取得工作區 vNet 對等的對等。</span><span class="sxs-lookup"><span data-stu-id="b55bc-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="b55bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b55bc-104">SYNTAX</span></span>

### <span data-ttu-id="b55bc-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="b55bc-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b55bc-106">獲取</span><span class="sxs-lookup"><span data-stu-id="b55bc-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b55bc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b55bc-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="b55bc-108">說明</span><span class="sxs-lookup"><span data-stu-id="b55bc-108">DESCRIPTION</span></span>
<span data-ttu-id="b55bc-109">取得工作區 vNet 對等的對等。</span><span class="sxs-lookup"><span data-stu-id="b55bc-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="b55bc-110">示例</span><span class="sxs-lookup"><span data-stu-id="b55bc-110">EXAMPLES</span></span>

### <span data-ttu-id="b55bc-111">範例1：列出 databricks 下的所有 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="b55bc-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="b55bc-112">這個命令會列出 databricks 下的所有 vnet 對等。</span><span class="sxs-lookup"><span data-stu-id="b55bc-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="b55bc-113">範例2：取得 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="b55bc-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="b55bc-114">這個命令會取得 vnet 對等。</span><span class="sxs-lookup"><span data-stu-id="b55bc-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="b55bc-115">範例3：透過物件取得 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="b55bc-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="b55bc-116">這個命令會透過物件取得 vnet 對等。</span><span class="sxs-lookup"><span data-stu-id="b55bc-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="b55bc-117">參數</span><span class="sxs-lookup"><span data-stu-id="b55bc-117">PARAMETERS</span></span>

### <span data-ttu-id="b55bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b55bc-118">-DefaultProfile</span></span>
<span data-ttu-id="b55bc-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b55bc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b55bc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b55bc-120">-InputObject</span></span>
<span data-ttu-id="b55bc-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b55bc-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b55bc-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b55bc-122">-Name</span></span>
<span data-ttu-id="b55bc-123">工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="b55bc-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="b55bc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b55bc-124">-PassThru</span></span>
<span data-ttu-id="b55bc-125">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="b55bc-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55bc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b55bc-126">-ResourceGroupName</span></span>
<span data-ttu-id="b55bc-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b55bc-127">The name of the resource group.</span></span>
<span data-ttu-id="b55bc-128">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b55bc-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b55bc-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b55bc-129">-SubscriptionId</span></span>
<span data-ttu-id="b55bc-130">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="b55bc-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b55bc-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b55bc-131">-WorkspaceName</span></span>
<span data-ttu-id="b55bc-132">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b55bc-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="b55bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55bc-133">CommonParameters</span></span>
<span data-ttu-id="b55bc-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b55bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55bc-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b55bc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55bc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b55bc-136">INPUTS</span></span>

### <span data-ttu-id="b55bc-137">IDatabricksIdentity （Databricks）的</span><span class="sxs-lookup"><span data-stu-id="b55bc-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="b55bc-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b55bc-138">OUTPUTS</span></span>

### <span data-ttu-id="b55bc-139">IVirtualNetworkPeering （Databricks）。 Api20180401。</span><span class="sxs-lookup"><span data-stu-id="b55bc-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="b55bc-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b55bc-140">NOTES</span></span>

<span data-ttu-id="b55bc-141">別名</span><span class="sxs-lookup"><span data-stu-id="b55bc-141">ALIASES</span></span>

<span data-ttu-id="b55bc-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b55bc-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b55bc-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b55bc-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b55bc-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b55bc-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b55bc-145">INPUTOBJECT <IDatabricksIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b55bc-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b55bc-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b55bc-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b55bc-147">`[PeeringName <String>]`： Workspace vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="b55bc-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="b55bc-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b55bc-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b55bc-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b55bc-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="b55bc-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b55bc-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b55bc-151">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b55bc-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="b55bc-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b55bc-152">RELATED LINKS</span></span>

