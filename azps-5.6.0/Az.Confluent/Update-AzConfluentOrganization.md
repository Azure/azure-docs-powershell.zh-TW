---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/update-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
ms.openlocfilehash: 7332d3154e87da2d9249dc16e3986efd636b737a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917062"
---
# <span data-ttu-id="6420d-101">Update-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="6420d-101">Update-AzConfluentOrganization</span></span>

## <span data-ttu-id="6420d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6420d-102">SYNOPSIS</span></span>
<span data-ttu-id="6420d-103">更新組織資源</span><span class="sxs-lookup"><span data-stu-id="6420d-103">Update Organization resource</span></span>

## <span data-ttu-id="6420d-104">語法</span><span class="sxs-lookup"><span data-stu-id="6420d-104">SYNTAX</span></span>

### <span data-ttu-id="6420d-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="6420d-105">UpdateExpanded (Default)</span></span>
```
Update-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6420d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6420d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConfluentOrganization -InputObject <IConfluentIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6420d-107">描述</span><span class="sxs-lookup"><span data-stu-id="6420d-107">DESCRIPTION</span></span>
<span data-ttu-id="6420d-108">更新組織資源</span><span class="sxs-lookup"><span data-stu-id="6420d-108">Update Organization resource</span></span>

## <span data-ttu-id="6420d-109">例子</span><span class="sxs-lookup"><span data-stu-id="6420d-109">EXAMPLES</span></span>

### <span data-ttu-id="6420d-110">範例 1：根據名稱更新不必要的組織</span><span class="sxs-lookup"><span data-stu-id="6420d-110">Example 1: Update a confluent organization by name</span></span>
```powershell
PS C:\> pdate-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Tag @{"key01" = "value01"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="6420d-111">此命令會根據名稱更新不必要的組織。</span><span class="sxs-lookup"><span data-stu-id="6420d-111">This command updates a confluent organization by name.</span></span>

### <span data-ttu-id="6420d-112">範例 2：根據管線更新匯流組織</span><span class="sxs-lookup"><span data-stu-id="6420d-112">Example 2: Update a confluent organization by pipeline</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Update-AzConfluentOrganization -Tag @{"key01" = "value01"; "key02"="value02"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="6420d-113">此命令會根據管線更新一個不必要的組織。</span><span class="sxs-lookup"><span data-stu-id="6420d-113">This command updates a confluent organization by pipeline.</span></span>

## <span data-ttu-id="6420d-114">參數</span><span class="sxs-lookup"><span data-stu-id="6420d-114">PARAMETERS</span></span>

### <span data-ttu-id="6420d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6420d-115">-DefaultProfile</span></span>
<span data-ttu-id="6420d-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6420d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6420d-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6420d-117">-InputObject</span></span>
<span data-ttu-id="6420d-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6420d-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6420d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6420d-119">-Name</span></span>
<span data-ttu-id="6420d-120">組織資源名稱</span><span class="sxs-lookup"><span data-stu-id="6420d-120">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6420d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6420d-121">-ResourceGroupName</span></span>
<span data-ttu-id="6420d-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="6420d-122">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6420d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6420d-123">-SubscriptionId</span></span>
<span data-ttu-id="6420d-124">Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="6420d-124">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6420d-125">-標記</span><span class="sxs-lookup"><span data-stu-id="6420d-125">-Tag</span></span>
<span data-ttu-id="6420d-126">ARM 資源標記</span><span class="sxs-lookup"><span data-stu-id="6420d-126">ARM resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6420d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="6420d-127">-Confirm</span></span>
<span data-ttu-id="6420d-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6420d-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6420d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6420d-129">-WhatIf</span></span>
<span data-ttu-id="6420d-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6420d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6420d-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6420d-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6420d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6420d-132">CommonParameters</span></span>
<span data-ttu-id="6420d-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6420d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6420d-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6420d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6420d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6420d-135">INPUTS</span></span>

### <span data-ttu-id="6420d-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="6420d-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="6420d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6420d-137">OUTPUTS</span></span>

### <span data-ttu-id="6420d-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="6420d-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="6420d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6420d-139">NOTES</span></span>

<span data-ttu-id="6420d-140">別名</span><span class="sxs-lookup"><span data-stu-id="6420d-140">ALIASES</span></span>

<span data-ttu-id="6420d-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6420d-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6420d-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6420d-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6420d-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6420d-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6420d-144">INPUTOBJECT： <IConfluentIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6420d-144">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6420d-145">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6420d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6420d-146">`[OrganizationName <String>]`：組織資源名稱</span><span class="sxs-lookup"><span data-stu-id="6420d-146">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="6420d-147">`[ResourceGroupName <String>]`：資源組名</span><span class="sxs-lookup"><span data-stu-id="6420d-147">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="6420d-148">`[SubscriptionId <String>]`：Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="6420d-148">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="6420d-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="6420d-149">RELATED LINKS</span></span>

