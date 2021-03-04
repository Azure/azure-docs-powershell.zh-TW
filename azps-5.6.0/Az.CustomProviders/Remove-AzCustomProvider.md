---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/remove-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProvider.md
ms.openlocfilehash: 87d04a30b5e04132f937d21b3585557efe71f4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914129"
---
# <span data-ttu-id="813b4-101">Remove-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="813b4-101">Remove-AzCustomProvider</span></span>

## <span data-ttu-id="813b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="813b4-102">SYNOPSIS</span></span>
<span data-ttu-id="813b4-103">刪除自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="813b4-103">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="813b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="813b4-104">SYNTAX</span></span>

### <span data-ttu-id="813b4-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="813b4-105">Delete (Default)</span></span>
```
Remove-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="813b4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="813b4-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="813b4-107">描述</span><span class="sxs-lookup"><span data-stu-id="813b4-107">DESCRIPTION</span></span>
<span data-ttu-id="813b4-108">刪除自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="813b4-108">Deletes the custom resource provider.</span></span>

## <span data-ttu-id="813b4-109">例子</span><span class="sxs-lookup"><span data-stu-id="813b4-109">EXAMPLES</span></span>

### <span data-ttu-id="813b4-110">範例 1：移除自訂提供者。</span><span class="sxs-lookup"><span data-stu-id="813b4-110">Example 1: Remove a custom provider.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
```

<span data-ttu-id="813b4-111">移除自訂提供者</span><span class="sxs-lookup"><span data-stu-id="813b4-111">Remove a custom provider</span></span>

### <span data-ttu-id="813b4-112">範例 2：使用 PassThru 移除自訂提供者</span><span class="sxs-lookup"><span data-stu-id="813b4-112">Example 2: Remove a custom provider with PassThru</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -PassThru

True
```

<span data-ttu-id="813b4-113">使用 PassThru 功能來表示成功或失敗，移除自訂提供者。</span><span class="sxs-lookup"><span data-stu-id="813b4-113">Remove a custom provider, using the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="813b4-114">參數</span><span class="sxs-lookup"><span data-stu-id="813b4-114">PARAMETERS</span></span>

### <span data-ttu-id="813b4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="813b4-115">-AsJob</span></span>
<span data-ttu-id="813b4-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="813b4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="813b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="813b4-117">-DefaultProfile</span></span>
<span data-ttu-id="813b4-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="813b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="813b4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="813b4-119">-InputObject</span></span>
<span data-ttu-id="813b4-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="813b4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="813b4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="813b4-121">-Name</span></span>
<span data-ttu-id="813b4-122">資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="813b4-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="813b4-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="813b4-123">-NoWait</span></span>
<span data-ttu-id="813b4-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="813b4-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="813b4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="813b4-125">-PassThru</span></span>
<span data-ttu-id="813b4-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="813b4-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="813b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="813b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="813b4-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="813b4-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="813b4-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="813b4-129">-SubscriptionId</span></span>
<span data-ttu-id="813b4-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="813b4-130">The Azure subscription ID.</span></span>
<span data-ttu-id="813b4-131">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="813b4-131">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="813b4-132">-確認</span><span class="sxs-lookup"><span data-stu-id="813b4-132">-Confirm</span></span>
<span data-ttu-id="813b4-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="813b4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="813b4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="813b4-134">-WhatIf</span></span>
<span data-ttu-id="813b4-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="813b4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="813b4-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="813b4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="813b4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="813b4-137">CommonParameters</span></span>
<span data-ttu-id="813b4-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="813b4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="813b4-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="813b4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="813b4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="813b4-140">INPUTS</span></span>

### <span data-ttu-id="813b4-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="813b4-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="813b4-142">輸出</span><span class="sxs-lookup"><span data-stu-id="813b4-142">OUTPUTS</span></span>

### <span data-ttu-id="813b4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="813b4-143">System.Boolean</span></span>

## <span data-ttu-id="813b4-144">筆記</span><span class="sxs-lookup"><span data-stu-id="813b4-144">NOTES</span></span>

<span data-ttu-id="813b4-145">別名</span><span class="sxs-lookup"><span data-stu-id="813b4-145">ALIASES</span></span>

<span data-ttu-id="813b4-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="813b4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="813b4-147">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="813b4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="813b4-148">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="813b4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="813b4-149">INPUTOBJECT： <ICustomProvidersIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="813b4-149">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="813b4-150">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="813b4-150">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="813b4-151">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="813b4-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="813b4-152">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="813b4-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="813b4-153">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="813b4-153">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="813b4-154">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="813b4-154">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="813b4-155">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="813b4-155">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="813b4-156">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="813b4-156">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="813b4-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="813b4-157">RELATED LINKS</span></span>

