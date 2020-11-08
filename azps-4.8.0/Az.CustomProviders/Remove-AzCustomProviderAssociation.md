---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/remove-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Remove-AzCustomProviderAssociation.md
ms.openlocfilehash: 708bac976e32c2af114576d971c05843fd58ef93
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136505"
---
# <span data-ttu-id="b3be5-101">Remove-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="b3be5-101">Remove-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="b3be5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b3be5-102">SYNOPSIS</span></span>
<span data-ttu-id="b3be5-103">刪除關聯。</span><span class="sxs-lookup"><span data-stu-id="b3be5-103">Delete an association.</span></span>

## <span data-ttu-id="b3be5-104">句法</span><span class="sxs-lookup"><span data-stu-id="b3be5-104">SYNTAX</span></span>

### <span data-ttu-id="b3be5-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b3be5-105">Delete (Default)</span></span>
```
Remove-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3be5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3be5-106">DeleteViaIdentity</span></span>
```
Remove-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3be5-107">說明</span><span class="sxs-lookup"><span data-stu-id="b3be5-107">DESCRIPTION</span></span>
<span data-ttu-id="b3be5-108">刪除關聯。</span><span class="sxs-lookup"><span data-stu-id="b3be5-108">Delete an association.</span></span>

## <span data-ttu-id="b3be5-109">示例</span><span class="sxs-lookup"><span data-stu-id="b3be5-109">EXAMPLES</span></span>

### <span data-ttu-id="b3be5-110">範例1：移除自訂提供者關聯。</span><span class="sxs-lookup"><span data-stu-id="b3be5-110">Example 1: Remove a custom provider association.</span></span>
```powershell
PS C:\> PS C:\> Remove-AzCustomProviderAssociation -Scope $id -Name Namespace.Type
```

<span data-ttu-id="b3be5-111">移除自訂提供者關聯。</span><span class="sxs-lookup"><span data-stu-id="b3be5-111">Remove a custom provider association.</span></span>

### <span data-ttu-id="b3be5-112">範例2：移除與管道的自訂提供者關聯</span><span class="sxs-lookup"><span data-stu-id="b3be5-112">Example 2: Remove a custom provider association with Piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProviderAssociation | Remove-AzCustomProviderAssociation -PassThru

True
```

<span data-ttu-id="b3be5-113">移除自訂提供者關聯，使用 [管道] 和 [PassThru] 功能來指示成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="b3be5-113">Remove a custom provider association, using piping and the PassThru feature to indicate success or failure.</span></span>

## <span data-ttu-id="b3be5-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3be5-114">PARAMETERS</span></span>

### <span data-ttu-id="b3be5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3be5-115">-AsJob</span></span>
<span data-ttu-id="b3be5-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="b3be5-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b3be5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3be5-117">-DefaultProfile</span></span>
<span data-ttu-id="b3be5-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3be5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3be5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3be5-119">-InputObject</span></span>
<span data-ttu-id="b3be5-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b3be5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b3be5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3be5-121">-Name</span></span>
<span data-ttu-id="b3be5-122">關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be5-122">The name of the association.</span></span>

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

### <span data-ttu-id="b3be5-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3be5-123">-NoWait</span></span>
<span data-ttu-id="b3be5-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="b3be5-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3be5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3be5-125">-PassThru</span></span>
<span data-ttu-id="b3be5-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="b3be5-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3be5-127">-範圍</span><span class="sxs-lookup"><span data-stu-id="b3be5-127">-Scope</span></span>
<span data-ttu-id="b3be5-128">關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="b3be5-128">The scope of the association.</span></span>

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

### <span data-ttu-id="b3be5-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b3be5-129">-Confirm</span></span>
<span data-ttu-id="b3be5-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b3be5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3be5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3be5-131">-WhatIf</span></span>
<span data-ttu-id="b3be5-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3be5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3be5-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3be5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3be5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3be5-134">CommonParameters</span></span>
<span data-ttu-id="b3be5-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b3be5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3be5-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b3be5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3be5-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b3be5-137">INPUTS</span></span>

### <span data-ttu-id="b3be5-138">ICustomProvidersIdentity （CustomProviders）的</span><span class="sxs-lookup"><span data-stu-id="b3be5-138">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="b3be5-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b3be5-139">OUTPUTS</span></span>

### <span data-ttu-id="b3be5-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b3be5-140">System.Boolean</span></span>

## <span data-ttu-id="b3be5-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b3be5-141">NOTES</span></span>

<span data-ttu-id="b3be5-142">別名</span><span class="sxs-lookup"><span data-stu-id="b3be5-142">ALIASES</span></span>

<span data-ttu-id="b3be5-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b3be5-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3be5-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b3be5-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3be5-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b3be5-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3be5-146">INPUTOBJECT <ICustomProvidersIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b3be5-146">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3be5-147">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be5-147">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="b3be5-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b3be5-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3be5-149">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be5-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b3be5-150">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3be5-150">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="b3be5-151">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="b3be5-151">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="b3be5-152">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b3be5-152">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b3be5-153">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="b3be5-153">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b3be5-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3be5-154">RELATED LINKS</span></span>

