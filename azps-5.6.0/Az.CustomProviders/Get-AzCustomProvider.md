---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 287472f89e7875411e287fa1315d5622a4c48a6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913961"
---
# <span data-ttu-id="7fe65-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="7fe65-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="7fe65-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7fe65-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe65-103">獲得自訂資源提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="7fe65-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="7fe65-104">語法</span><span class="sxs-lookup"><span data-stu-id="7fe65-104">SYNTAX</span></span>

### <span data-ttu-id="7fe65-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="7fe65-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fe65-106">獲取</span><span class="sxs-lookup"><span data-stu-id="7fe65-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fe65-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7fe65-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7fe65-108">清單</span><span class="sxs-lookup"><span data-stu-id="7fe65-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fe65-109">描述</span><span class="sxs-lookup"><span data-stu-id="7fe65-109">DESCRIPTION</span></span>
<span data-ttu-id="7fe65-110">獲得自訂資源提供者的清單。</span><span class="sxs-lookup"><span data-stu-id="7fe65-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="7fe65-111">例子</span><span class="sxs-lookup"><span data-stu-id="7fe65-111">EXAMPLES</span></span>

### <span data-ttu-id="7fe65-112">範例 1：列出訂閱中所有的自訂提供者</span><span class="sxs-lookup"><span data-stu-id="7fe65-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="7fe65-113">列出訂閱中所有的自訂提供者</span><span class="sxs-lookup"><span data-stu-id="7fe65-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="7fe65-114">範例 2：取得單一自訂提供者</span><span class="sxs-lookup"><span data-stu-id="7fe65-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

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

<span data-ttu-id="7fe65-115">獲得單一自訂提供者的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="7fe65-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="7fe65-116">使用Format-List顯示畫面上的物件詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7fe65-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="7fe65-117">參數</span><span class="sxs-lookup"><span data-stu-id="7fe65-117">PARAMETERS</span></span>

### <span data-ttu-id="7fe65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe65-118">-DefaultProfile</span></span>
<span data-ttu-id="7fe65-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fe65-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fe65-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fe65-120">-InputObject</span></span>
<span data-ttu-id="7fe65-121">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7fe65-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe65-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7fe65-122">-Name</span></span>
<span data-ttu-id="7fe65-123">資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe65-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe65-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fe65-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fe65-125">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe65-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="7fe65-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fe65-126">-SubscriptionId</span></span>
<span data-ttu-id="7fe65-127">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fe65-127">The Azure subscription ID.</span></span>
<span data-ttu-id="7fe65-128">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="7fe65-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="7fe65-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe65-129">CommonParameters</span></span>
<span data-ttu-id="7fe65-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7fe65-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe65-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fe65-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe65-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7fe65-132">INPUTS</span></span>

### <span data-ttu-id="7fe65-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="7fe65-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="7fe65-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7fe65-134">OUTPUTS</span></span>

### <span data-ttu-id="7fe65-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="7fe65-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="7fe65-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7fe65-136">NOTES</span></span>

<span data-ttu-id="7fe65-137">別名</span><span class="sxs-lookup"><span data-stu-id="7fe65-137">ALIASES</span></span>

<span data-ttu-id="7fe65-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="7fe65-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7fe65-139">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="7fe65-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fe65-140">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="7fe65-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7fe65-141">INPUTOBJECT： <ICustomProvidersIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="7fe65-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fe65-142">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe65-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="7fe65-143">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="7fe65-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fe65-144">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe65-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="7fe65-145">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fe65-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="7fe65-146">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="7fe65-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="7fe65-147">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7fe65-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="7fe65-148">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="7fe65-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="7fe65-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fe65-149">RELATED LINKS</span></span>

