---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: a5654fa0974accf4319df4cbbd08ef220fa7ad9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905541"
---
# <span data-ttu-id="a1e4e-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="a1e4e-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="a1e4e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e4e-103">獲得工作區 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="a1e4e-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1e4e-104">SYNTAX</span></span>

### <span data-ttu-id="a1e4e-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="a1e4e-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a1e4e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a1e4e-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a1e4e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a1e4e-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a1e4e-108">描述</span><span class="sxs-lookup"><span data-stu-id="a1e4e-108">DESCRIPTION</span></span>
<span data-ttu-id="a1e4e-109">獲得工作區 vNet 對等。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="a1e4e-110">例子</span><span class="sxs-lookup"><span data-stu-id="a1e4e-110">EXAMPLES</span></span>

### <span data-ttu-id="a1e4e-111">範例 1：在 datab一s 下列出所有 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="a1e4e-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="a1e4e-112">此命令會列出資料樹下的所有 vnet 對等。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="a1e4e-113">範例 2：取得 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="a1e4e-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="a1e4e-114">此命令會進行 vnet 對等。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="a1e4e-115">範例 3：根據物件取得 vnet 對等</span><span class="sxs-lookup"><span data-stu-id="a1e4e-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="a1e4e-116">此命令會按物件進行 vnet 對等。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="a1e4e-117">參數</span><span class="sxs-lookup"><span data-stu-id="a1e4e-117">PARAMETERS</span></span>

### <span data-ttu-id="a1e4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e4e-118">-DefaultProfile</span></span>
<span data-ttu-id="a1e4e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1e4e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1e4e-120">-InputObject</span></span>
<span data-ttu-id="a1e4e-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a1e4e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1e4e-122">-Name</span></span>
<span data-ttu-id="a1e4e-123">工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="a1e4e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1e4e-124">-PassThru</span></span>
<span data-ttu-id="a1e4e-125">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="a1e4e-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a1e4e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e4e-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1e4e-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-127">The name of the resource group.</span></span>
<span data-ttu-id="a1e4e-128">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a1e4e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1e4e-129">-SubscriptionId</span></span>
<span data-ttu-id="a1e4e-130">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a1e4e-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a1e4e-131">-WorkspaceName</span></span>
<span data-ttu-id="a1e4e-132">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="a1e4e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e4e-133">CommonParameters</span></span>
<span data-ttu-id="a1e4e-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e4e-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1e4e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e4e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a1e4e-136">INPUTS</span></span>

### <span data-ttu-id="a1e4e-137">Microsoft.Azure.PowerShell.Cmdlets.Databuvs.models.IDatab一sIdentity</span><span class="sxs-lookup"><span data-stu-id="a1e4e-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="a1e4e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="a1e4e-138">OUTPUTS</span></span>

### <span data-ttu-id="a1e4e-139">Microsoft.Azure.PowerShell.Cmdlets.Databworks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="a1e4e-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="a1e4e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="a1e4e-140">NOTES</span></span>

<span data-ttu-id="a1e4e-141">別名</span><span class="sxs-lookup"><span data-stu-id="a1e4e-141">ALIASES</span></span>

<span data-ttu-id="a1e4e-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a1e4e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a1e4e-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1e4e-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a1e4e-145">INPUTOBJECT： <IDatabricksIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="a1e4e-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a1e4e-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="a1e4e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a1e4e-147">`[PeeringName <String>]`：工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="a1e4e-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a1e4e-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="a1e4e-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a1e4e-151">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1e4e-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="a1e4e-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1e4e-152">RELATED LINKS</span></span>

