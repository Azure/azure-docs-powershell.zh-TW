---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 0f124d818b95928f12cdc71f60c436f5691f8151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914118"
---
# <span data-ttu-id="b1c15-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="b1c15-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="b1c15-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1c15-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c15-103">更新現有的自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b1c15-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="b1c15-104">目前唯一可以透過修補程式更新的值是標記。</span><span class="sxs-lookup"><span data-stu-id="b1c15-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="b1c15-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1c15-105">SYNTAX</span></span>

### <span data-ttu-id="b1c15-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b1c15-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b1c15-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b1c15-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1c15-108">描述</span><span class="sxs-lookup"><span data-stu-id="b1c15-108">DESCRIPTION</span></span>
<span data-ttu-id="b1c15-109">更新現有的自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b1c15-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="b1c15-110">目前唯一可以透過修補程式更新的值是標記。</span><span class="sxs-lookup"><span data-stu-id="b1c15-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="b1c15-111">例子</span><span class="sxs-lookup"><span data-stu-id="b1c15-111">EXAMPLES</span></span>

### <span data-ttu-id="b1c15-112">範例 1：新增標記至自訂提供者</span><span class="sxs-lookup"><span data-stu-id="b1c15-112">Example 1: Add Tags to a custom Provider</span></span>
```powershell
PS C:\> Update-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type -Tag @{MyTag="MyValue"} | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :
```

<span data-ttu-id="b1c15-113">更新自訂提供者的標記。</span><span class="sxs-lookup"><span data-stu-id="b1c15-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="b1c15-114">範例 2：使用管線更新自訂提供者</span><span class="sxs-lookup"><span data-stu-id="b1c15-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="b1c15-115">使用管線更新自訂提供者。</span><span class="sxs-lookup"><span data-stu-id="b1c15-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="b1c15-116">參數</span><span class="sxs-lookup"><span data-stu-id="b1c15-116">PARAMETERS</span></span>

### <span data-ttu-id="b1c15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c15-117">-DefaultProfile</span></span>
<span data-ttu-id="b1c15-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1c15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1c15-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1c15-119">-InputObject</span></span>
<span data-ttu-id="b1c15-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b1c15-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1c15-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1c15-121">-Name</span></span>
<span data-ttu-id="b1c15-122">資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1c15-122">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1c15-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c15-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1c15-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1c15-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1c15-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1c15-125">-SubscriptionId</span></span>
<span data-ttu-id="b1c15-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1c15-126">The Azure subscription ID.</span></span>
<span data-ttu-id="b1c15-127">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="b1c15-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="b1c15-128">-標記</span><span class="sxs-lookup"><span data-stu-id="b1c15-128">-Tag</span></span>
<span data-ttu-id="b1c15-129">資源標記</span><span class="sxs-lookup"><span data-stu-id="b1c15-129">Resource tags</span></span>

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

### <span data-ttu-id="b1c15-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b1c15-130">-Confirm</span></span>
<span data-ttu-id="b1c15-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1c15-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1c15-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1c15-132">-WhatIf</span></span>
<span data-ttu-id="b1c15-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1c15-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1c15-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1c15-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1c15-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c15-135">CommonParameters</span></span>
<span data-ttu-id="b1c15-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1c15-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c15-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1c15-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c15-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b1c15-138">INPUTS</span></span>

### <span data-ttu-id="b1c15-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="b1c15-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="b1c15-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b1c15-140">OUTPUTS</span></span>

### <span data-ttu-id="b1c15-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="b1c15-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="b1c15-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b1c15-142">NOTES</span></span>

<span data-ttu-id="b1c15-143">別名</span><span class="sxs-lookup"><span data-stu-id="b1c15-143">ALIASES</span></span>

<span data-ttu-id="b1c15-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b1c15-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1c15-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b1c15-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1c15-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b1c15-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1c15-147">INPUTOBJECT： <ICustomProvidersIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b1c15-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1c15-148">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1c15-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="b1c15-149">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b1c15-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1c15-150">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1c15-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b1c15-151">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1c15-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="b1c15-152">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="b1c15-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="b1c15-153">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1c15-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="b1c15-154">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="b1c15-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="b1c15-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1c15-155">RELATED LINKS</span></span>

