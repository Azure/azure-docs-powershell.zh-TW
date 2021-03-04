---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/remove-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Remove-AzConfluentOrganization.md
ms.openlocfilehash: d35de003bd4822758fd75c7dbbcf616ebecbbccb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917061"
---
# <span data-ttu-id="5ef1a-101">Remove-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="5ef1a-101">Remove-AzConfluentOrganization</span></span>

## <span data-ttu-id="5ef1a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ef1a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef1a-103">刪除組織資源</span><span class="sxs-lookup"><span data-stu-id="5ef1a-103">Delete Organization resource</span></span>

## <span data-ttu-id="5ef1a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ef1a-104">SYNTAX</span></span>

### <span data-ttu-id="5ef1a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="5ef1a-105">Delete (Default)</span></span>
```
Remove-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5ef1a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ef1a-106">DeleteViaIdentity</span></span>
```
Remove-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5ef1a-107">描述</span><span class="sxs-lookup"><span data-stu-id="5ef1a-107">DESCRIPTION</span></span>
<span data-ttu-id="5ef1a-108">刪除組織資源</span><span class="sxs-lookup"><span data-stu-id="5ef1a-108">Delete Organization resource</span></span>

## <span data-ttu-id="5ef1a-109">例子</span><span class="sxs-lookup"><span data-stu-id="5ef1a-109">EXAMPLES</span></span>

### <span data-ttu-id="5ef1a-110">範例 1：根據名稱移除不必要的組織</span><span class="sxs-lookup"><span data-stu-id="5ef1a-110">Example 1: Remove a confluent organization by name</span></span>
```powershell
PS C:\> Remove-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

```

<span data-ttu-id="5ef1a-111">此命令會根據名稱移除不必要的組織</span><span class="sxs-lookup"><span data-stu-id="5ef1a-111">This command removes a confluent organization by name</span></span>

### <span data-ttu-id="5ef1a-112">範例 2：根據管線移除不必要的組織</span><span class="sxs-lookup"><span data-stu-id="5ef1a-112">Example 2: Remove a confluent organization by pipeline</span></span>
```powershell
PS C:\>  Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Remove-AzConfluentOrganization

```

<span data-ttu-id="5ef1a-113">此命令會根據管線移除不必要的組織。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-113">This command removes a confluent organization by pipeline.</span></span>

## <span data-ttu-id="5ef1a-114">參數</span><span class="sxs-lookup"><span data-stu-id="5ef1a-114">PARAMETERS</span></span>

### <span data-ttu-id="5ef1a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ef1a-115">-AsJob</span></span>
<span data-ttu-id="5ef1a-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="5ef1a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5ef1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef1a-117">-DefaultProfile</span></span>
<span data-ttu-id="5ef1a-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ef1a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ef1a-119">-InputObject</span></span>
<span data-ttu-id="5ef1a-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef1a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ef1a-121">-Name</span></span>
<span data-ttu-id="5ef1a-122">組織資源名稱</span><span class="sxs-lookup"><span data-stu-id="5ef1a-122">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef1a-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5ef1a-123">-NoWait</span></span>
<span data-ttu-id="5ef1a-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="5ef1a-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5ef1a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ef1a-125">-PassThru</span></span>
<span data-ttu-id="5ef1a-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="5ef1a-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5ef1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ef1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ef1a-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="5ef1a-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef1a-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ef1a-129">-SubscriptionId</span></span>
<span data-ttu-id="5ef1a-130">Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="5ef1a-130">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ef1a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="5ef1a-131">-Confirm</span></span>
<span data-ttu-id="5ef1a-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ef1a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ef1a-133">-WhatIf</span></span>
<span data-ttu-id="5ef1a-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ef1a-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ef1a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef1a-136">CommonParameters</span></span>
<span data-ttu-id="5ef1a-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef1a-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ef1a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef1a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5ef1a-139">INPUTS</span></span>

### <span data-ttu-id="5ef1a-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="5ef1a-140">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="5ef1a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5ef1a-141">OUTPUTS</span></span>

### <span data-ttu-id="5ef1a-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ef1a-142">System.Boolean</span></span>

## <span data-ttu-id="5ef1a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5ef1a-143">NOTES</span></span>

<span data-ttu-id="5ef1a-144">別名</span><span class="sxs-lookup"><span data-stu-id="5ef1a-144">ALIASES</span></span>

<span data-ttu-id="5ef1a-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5ef1a-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ef1a-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ef1a-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5ef1a-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ef1a-148">INPUTOBJECT： <IConfluentIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5ef1a-148">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ef1a-149">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="5ef1a-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ef1a-150">`[OrganizationName <String>]`：組織資源名稱</span><span class="sxs-lookup"><span data-stu-id="5ef1a-150">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="5ef1a-151">`[ResourceGroupName <String>]`：資源組名</span><span class="sxs-lookup"><span data-stu-id="5ef1a-151">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="5ef1a-152">`[SubscriptionId <String>]`：Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="5ef1a-152">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="5ef1a-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ef1a-153">RELATED LINKS</span></span>

