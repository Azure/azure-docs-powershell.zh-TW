---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/update-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Update-AzCustomProvider.md
ms.openlocfilehash: 6691586d454952f92d71a26d5b8ed02904f37bf8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285378"
---
# <span data-ttu-id="5c0ec-101">Update-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="5c0ec-101">Update-AzCustomProvider</span></span>

## <span data-ttu-id="5c0ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0ec-103">更新現有的自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-103">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="5c0ec-104">只能透過修補程式更新的值為標籤。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-104">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="5c0ec-105">句法</span><span class="sxs-lookup"><span data-stu-id="5c0ec-105">SYNTAX</span></span>

### <span data-ttu-id="5c0ec-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="5c0ec-106">UpdateExpanded (Default)</span></span>
```
Update-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5c0ec-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5c0ec-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5c0ec-108">說明</span><span class="sxs-lookup"><span data-stu-id="5c0ec-108">DESCRIPTION</span></span>
<span data-ttu-id="5c0ec-109">更新現有的自訂資源提供者。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-109">Updates an existing custom resource provider.</span></span>
<span data-ttu-id="5c0ec-110">只能透過修補程式更新的值為標籤。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-110">The only value that can be updated via PATCH currently is the tags.</span></span>

## <span data-ttu-id="5c0ec-111">示例</span><span class="sxs-lookup"><span data-stu-id="5c0ec-111">EXAMPLES</span></span>

### <span data-ttu-id="5c0ec-112">範例1：新增標籤至自訂提供者</span><span class="sxs-lookup"><span data-stu-id="5c0ec-112">Example 1: Add Tags to a custom Provider</span></span>
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

<span data-ttu-id="5c0ec-113">更新自訂提供者的標記。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-113">Update the tags of a custom provider.</span></span>

### <span data-ttu-id="5c0ec-114">範例2：使用管道更新自訂提供者</span><span class="sxs-lookup"><span data-stu-id="5c0ec-114">Example 2: Update custom provider with piping</span></span>
```powershell
PS C:\> PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Update-AzCustomProvider -Tag @{MyTag="MyValue"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="5c0ec-115">使用管道更新自訂提供者。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-115">Update a custom provider using piping.</span></span>

## <span data-ttu-id="5c0ec-116">參數</span><span class="sxs-lookup"><span data-stu-id="5c0ec-116">PARAMETERS</span></span>

### <span data-ttu-id="5c0ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0ec-117">-DefaultProfile</span></span>
<span data-ttu-id="5c0ec-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c0ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c0ec-119">-InputObject</span></span>
<span data-ttu-id="5c0ec-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5c0ec-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c0ec-121">-Name</span></span>
<span data-ttu-id="5c0ec-122">資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-122">The name of the resource provider.</span></span>

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

### <span data-ttu-id="5c0ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c0ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="5c0ec-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5c0ec-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c0ec-125">-SubscriptionId</span></span>
<span data-ttu-id="5c0ec-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-126">The Azure subscription ID.</span></span>
<span data-ttu-id="5c0ec-127">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="5c0ec-127">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="5c0ec-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c0ec-128">-Tag</span></span>
<span data-ttu-id="5c0ec-129">資源標記</span><span class="sxs-lookup"><span data-stu-id="5c0ec-129">Resource tags</span></span>

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

### <span data-ttu-id="5c0ec-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5c0ec-130">-Confirm</span></span>
<span data-ttu-id="5c0ec-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c0ec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c0ec-132">-WhatIf</span></span>
<span data-ttu-id="5c0ec-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c0ec-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c0ec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0ec-135">CommonParameters</span></span>
<span data-ttu-id="5c0ec-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0ec-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0ec-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5c0ec-138">INPUTS</span></span>

### <span data-ttu-id="5c0ec-139">ICustomProvidersIdentity （CustomProviders）的</span><span class="sxs-lookup"><span data-stu-id="5c0ec-139">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="5c0ec-140">輸出</span><span class="sxs-lookup"><span data-stu-id="5c0ec-140">OUTPUTS</span></span>

### <span data-ttu-id="5c0ec-141">ICustomRpManifest （CustomProviders）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-141">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="5c0ec-142">筆記</span><span class="sxs-lookup"><span data-stu-id="5c0ec-142">NOTES</span></span>

<span data-ttu-id="5c0ec-143">別名</span><span class="sxs-lookup"><span data-stu-id="5c0ec-143">ALIASES</span></span>

<span data-ttu-id="5c0ec-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5c0ec-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5c0ec-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c0ec-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5c0ec-147">INPUTOBJECT <ICustomProvidersIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5c0ec-147">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c0ec-148">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-148">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="5c0ec-149">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="5c0ec-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c0ec-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5c0ec-151">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-151">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="5c0ec-152">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-152">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="5c0ec-153">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="5c0ec-153">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="5c0ec-154">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="5c0ec-154">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="5c0ec-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c0ec-155">RELATED LINKS</span></span>

