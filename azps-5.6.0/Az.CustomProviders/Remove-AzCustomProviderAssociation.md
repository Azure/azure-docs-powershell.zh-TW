---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 6d3a6863044722be49efb78a71e3e0fbe82db5e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914125"
---
# <span data-ttu-id="9a617-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="9a617-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="9a617-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9a617-102">SYNOPSIS</span></span>
<span data-ttu-id="9a617-103">刪除關聯。</span><span class="sxs-lookup"><span data-stu-id="9a617-103">Delete an association.</span></span>

## <span data-ttu-id="9a617-104">語法</span><span class="sxs-lookup"><span data-stu-id="9a617-104">SYNTAX</span></span>

### <span data-ttu-id="9a617-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="9a617-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9a617-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a617-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a617-107">描述</span><span class="sxs-lookup"><span data-stu-id="9a617-107">DESCRIPTION</span></span>
<span data-ttu-id="9a617-108">刪除關聯。</span><span class="sxs-lookup"><span data-stu-id="9a617-108">Delete an association.</span></span>

## <span data-ttu-id="9a617-109">例子</span><span class="sxs-lookup"><span data-stu-id="9a617-109">EXAMPLES</span></span>

### <span data-ttu-id="9a617-110">範例 1：移除自訂提供者關聯。</span><span class="sxs-lookup"><span data-stu-id="9a617-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="9a617-111">移除自訂提供者關聯。</span><span class="sxs-lookup"><span data-stu-id="9a617-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="9a617-112">範例 2：移除自訂提供者與管道的關聯</span><span class="sxs-lookup"><span data-stu-id="9a617-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="9a617-113">移除自訂提供者關聯，使用管線和 PassThru 功能來表示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="9a617-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="9a617-114">參數</span><span class="sxs-lookup"><span data-stu-id="9a617-114">PARAMETERS</span></span>

### <span data-ttu-id="9a617-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a617-115">-AsJob</span></span>
<span data-ttu-id="9a617-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="9a617-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9a617-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a617-117">-DefaultProfile</span></span>
<span data-ttu-id="9a617-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a617-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a617-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a617-119">-InputObject</span></span>
<span data-ttu-id="9a617-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9a617-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9a617-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a617-121">-Name</span></span>
<span data-ttu-id="9a617-122">關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a617-122">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a617-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9a617-123">-NoWait</span></span>
<span data-ttu-id="9a617-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="9a617-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9a617-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a617-125">-PassThru</span></span>
<span data-ttu-id="9a617-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="9a617-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9a617-127">-範圍</span><span class="sxs-lookup"><span data-stu-id="9a617-127">-Scope</span></span>
<span data-ttu-id="9a617-128">關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="9a617-128">The scope of the association.</span></span>

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

### <span data-ttu-id="9a617-129">-確認</span><span class="sxs-lookup"><span data-stu-id="9a617-129">-Confirm</span></span>
<span data-ttu-id="9a617-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9a617-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a617-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a617-131">-WhatIf</span></span>
<span data-ttu-id="9a617-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a617-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a617-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a617-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a617-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a617-134">CommonParameters</span></span>
<span data-ttu-id="9a617-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9a617-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a617-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a617-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a617-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9a617-137">INPUTS</span></span>

### <span data-ttu-id="9a617-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="9a617-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="9a617-139">輸出</span><span class="sxs-lookup"><span data-stu-id="9a617-139">OUTPUTS</span></span>

### <span data-ttu-id="9a617-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a617-140">System.Boolean</span></span>

## <span data-ttu-id="9a617-141">筆記</span><span class="sxs-lookup"><span data-stu-id="9a617-141">NOTES</span></span>

<span data-ttu-id="9a617-142">別名</span><span class="sxs-lookup"><span data-stu-id="9a617-142">ALIASES</span></span>

<span data-ttu-id="9a617-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9a617-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a617-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9a617-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a617-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9a617-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a617-146">INPUTOBJECT： <ICustomProvidersIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9a617-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a617-147">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a617-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="9a617-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="9a617-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a617-149">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a617-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="9a617-150">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a617-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="9a617-151">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="9a617-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="9a617-152">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a617-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="9a617-153">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="9a617-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="9a617-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a617-154">RELATED LINKS</span></span>

