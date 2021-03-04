---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: ec44b1ace55a36ebaa56c8b0242db485581c5e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905538"
---
# <span data-ttu-id="5f46a-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="5f46a-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="5f46a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5f46a-102">SYNOPSIS</span></span>
<span data-ttu-id="5f46a-103">獲得工作區。</span><span class="sxs-lookup"><span data-stu-id="5f46a-103">Gets the workspace.</span></span>

## <span data-ttu-id="5f46a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5f46a-104">SYNTAX</span></span>

### <span data-ttu-id="5f46a-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="5f46a-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f46a-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5f46a-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f46a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5f46a-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5f46a-108">清單</span><span class="sxs-lookup"><span data-stu-id="5f46a-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5f46a-109">描述</span><span class="sxs-lookup"><span data-stu-id="5f46a-109">DESCRIPTION</span></span>
<span data-ttu-id="5f46a-110">獲得工作區。</span><span class="sxs-lookup"><span data-stu-id="5f46a-110">Gets the workspace.</span></span>

## <span data-ttu-id="5f46a-111">例子</span><span class="sxs-lookup"><span data-stu-id="5f46a-111">EXAMPLES</span></span>

### <span data-ttu-id="5f46a-112">範例 1：使用名稱取得 Datab一s 工作區</span><span class="sxs-lookup"><span data-stu-id="5f46a-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="5f46a-113">此命令會獲得資源群組中的 Datab一s 工作區。</span><span class="sxs-lookup"><span data-stu-id="5f46a-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="5f46a-114">範例 2：列出訂閱中所有的 Datab一s 工作區</span><span class="sxs-lookup"><span data-stu-id="5f46a-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="5f46a-115">此命令會列出訂閱中所有 Datab一s 工作區。</span><span class="sxs-lookup"><span data-stu-id="5f46a-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="5f46a-116">範例 3：列出資源群組中所有 Datab一s 工作區</span><span class="sxs-lookup"><span data-stu-id="5f46a-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="5f46a-117">此命令會列出資源群組中所有 Datab workspaces。</span><span class="sxs-lookup"><span data-stu-id="5f46a-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="5f46a-118">參數</span><span class="sxs-lookup"><span data-stu-id="5f46a-118">PARAMETERS</span></span>

### <span data-ttu-id="5f46a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f46a-119">-DefaultProfile</span></span>
<span data-ttu-id="5f46a-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5f46a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f46a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f46a-121">-InputObject</span></span>
<span data-ttu-id="5f46a-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5f46a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5f46a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="5f46a-123">-Name</span></span>
<span data-ttu-id="5f46a-124">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f46a-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f46a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f46a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5f46a-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f46a-126">The name of the resource group.</span></span>
<span data-ttu-id="5f46a-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5f46a-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5f46a-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5f46a-128">-SubscriptionId</span></span>
<span data-ttu-id="5f46a-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f46a-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f46a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f46a-130">CommonParameters</span></span>
<span data-ttu-id="5f46a-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5f46a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f46a-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f46a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f46a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5f46a-133">INPUTS</span></span>

### <span data-ttu-id="5f46a-134">Microsoft.Azure.PowerShell.Cmdlets.Databuvs.models.IDatab一sIdentity</span><span class="sxs-lookup"><span data-stu-id="5f46a-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="5f46a-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5f46a-135">OUTPUTS</span></span>

### <span data-ttu-id="5f46a-136">Microsoft.Azure.PowerShell.Cmdlets.Databworks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="5f46a-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="5f46a-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5f46a-137">NOTES</span></span>

<span data-ttu-id="5f46a-138">別名</span><span class="sxs-lookup"><span data-stu-id="5f46a-138">ALIASES</span></span>

<span data-ttu-id="5f46a-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5f46a-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5f46a-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5f46a-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5f46a-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5f46a-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5f46a-142">INPUTOBJECT： <IDatabricksIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5f46a-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5f46a-143">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="5f46a-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5f46a-144">`[PeeringName <String>]`：工作區 vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f46a-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="5f46a-145">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f46a-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5f46a-146">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="5f46a-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="5f46a-147">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f46a-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5f46a-148">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="5f46a-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="5f46a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f46a-149">RELATED LINKS</span></span>

