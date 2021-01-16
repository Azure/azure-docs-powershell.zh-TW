---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283956"
---
# <span data-ttu-id="c0489-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0489-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="c0489-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c0489-102">SYNOPSIS</span></span>
<span data-ttu-id="c0489-103">取得工作區。</span><span class="sxs-lookup"><span data-stu-id="c0489-103">Gets the workspace.</span></span>

## <span data-ttu-id="c0489-104">句法</span><span class="sxs-lookup"><span data-stu-id="c0489-104">SYNTAX</span></span>

### <span data-ttu-id="c0489-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="c0489-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c0489-106">獲取</span><span class="sxs-lookup"><span data-stu-id="c0489-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c0489-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c0489-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c0489-108">清單</span><span class="sxs-lookup"><span data-stu-id="c0489-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c0489-109">說明</span><span class="sxs-lookup"><span data-stu-id="c0489-109">DESCRIPTION</span></span>
<span data-ttu-id="c0489-110">取得工作區。</span><span class="sxs-lookup"><span data-stu-id="c0489-110">Gets the workspace.</span></span>

## <span data-ttu-id="c0489-111">示例</span><span class="sxs-lookup"><span data-stu-id="c0489-111">EXAMPLES</span></span>

### <span data-ttu-id="c0489-112">範例1：取得名稱為 Databricks 的工作區</span><span class="sxs-lookup"><span data-stu-id="c0489-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="c0489-113">這個命令會取得資源群組中的 Databricks 工作區。</span><span class="sxs-lookup"><span data-stu-id="c0489-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="c0489-114">範例2：列出訂閱中的所有 Databricks 工作區</span><span class="sxs-lookup"><span data-stu-id="c0489-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="c0489-115">這個命令會列出訂閱中的所有 Databricks 工作區。</span><span class="sxs-lookup"><span data-stu-id="c0489-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="c0489-116">範例3：列出資源群組中的所有 Databricks 工作區</span><span class="sxs-lookup"><span data-stu-id="c0489-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="c0489-117">這個命令會列出資源群組中的所有 Databricks 工作區。</span><span class="sxs-lookup"><span data-stu-id="c0489-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="c0489-118">參數</span><span class="sxs-lookup"><span data-stu-id="c0489-118">PARAMETERS</span></span>

### <span data-ttu-id="c0489-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0489-119">-DefaultProfile</span></span>
<span data-ttu-id="c0489-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0489-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0489-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0489-121">-InputObject</span></span>
<span data-ttu-id="c0489-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c0489-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c0489-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0489-123">-Name</span></span>
<span data-ttu-id="c0489-124">工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0489-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="c0489-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0489-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0489-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0489-126">The name of the resource group.</span></span>
<span data-ttu-id="c0489-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c0489-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c0489-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0489-128">-SubscriptionId</span></span>
<span data-ttu-id="c0489-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="c0489-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c0489-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0489-130">CommonParameters</span></span>
<span data-ttu-id="c0489-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c0489-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0489-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c0489-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0489-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c0489-133">INPUTS</span></span>

### <span data-ttu-id="c0489-134">IDatabricksIdentity （Databricks）的</span><span class="sxs-lookup"><span data-stu-id="c0489-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="c0489-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c0489-135">OUTPUTS</span></span>

### <span data-ttu-id="c0489-136">IWorkspace （Databricks）。 Api20180401。</span><span class="sxs-lookup"><span data-stu-id="c0489-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="c0489-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c0489-137">NOTES</span></span>

<span data-ttu-id="c0489-138">別名</span><span class="sxs-lookup"><span data-stu-id="c0489-138">ALIASES</span></span>

<span data-ttu-id="c0489-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c0489-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0489-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c0489-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0489-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c0489-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0489-142">INPUTOBJECT <IDatabricksIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c0489-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c0489-143">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c0489-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0489-144">`[PeeringName <String>]`： Workspace vNet 對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0489-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="c0489-145">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0489-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c0489-146">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c0489-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="c0489-147">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0489-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c0489-148">`[WorkspaceName <String>]`：工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0489-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="c0489-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0489-149">RELATED LINKS</span></span>

