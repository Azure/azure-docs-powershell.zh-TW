---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285391"
---
# <span data-ttu-id="831b6-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="831b6-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="831b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="831b6-102">SYNOPSIS</span></span>
<span data-ttu-id="831b6-103">取得自訂資源提供者資訊清單。</span><span class="sxs-lookup"><span data-stu-id="831b6-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="831b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="831b6-104">SYNTAX</span></span>

### <span data-ttu-id="831b6-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="831b6-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="831b6-106">獲取</span><span class="sxs-lookup"><span data-stu-id="831b6-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="831b6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="831b6-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="831b6-108">清單</span><span class="sxs-lookup"><span data-stu-id="831b6-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="831b6-109">說明</span><span class="sxs-lookup"><span data-stu-id="831b6-109">DESCRIPTION</span></span>
<span data-ttu-id="831b6-110">取得自訂資源提供者資訊清單。</span><span class="sxs-lookup"><span data-stu-id="831b6-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="831b6-111">示例</span><span class="sxs-lookup"><span data-stu-id="831b6-111">EXAMPLES</span></span>

### <span data-ttu-id="831b6-112">範例1：列出訂閱中的所有自訂提供者</span><span class="sxs-lookup"><span data-stu-id="831b6-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="831b6-113">列出訂閱中的所有自訂提供者</span><span class="sxs-lookup"><span data-stu-id="831b6-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="831b6-114">範例2：取得單一的自訂提供者</span><span class="sxs-lookup"><span data-stu-id="831b6-114">Example 2: Get a single custom provider</span></span>
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

<span data-ttu-id="831b6-115">取得單一自訂提供者的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="831b6-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="831b6-116">使用 Format-List 在畫面上顯示物件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="831b6-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="831b6-117">參數</span><span class="sxs-lookup"><span data-stu-id="831b6-117">PARAMETERS</span></span>

### <span data-ttu-id="831b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831b6-118">-DefaultProfile</span></span>
<span data-ttu-id="831b6-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="831b6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="831b6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="831b6-120">-InputObject</span></span>
<span data-ttu-id="831b6-121">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="831b6-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="831b6-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="831b6-122">-Name</span></span>
<span data-ttu-id="831b6-123">資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="831b6-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="831b6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="831b6-124">-ResourceGroupName</span></span>
<span data-ttu-id="831b6-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="831b6-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="831b6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="831b6-126">-SubscriptionId</span></span>
<span data-ttu-id="831b6-127">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="831b6-127">The Azure subscription ID.</span></span>
<span data-ttu-id="831b6-128">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="831b6-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="831b6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831b6-129">CommonParameters</span></span>
<span data-ttu-id="831b6-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="831b6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831b6-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="831b6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831b6-132">輸入</span><span class="sxs-lookup"><span data-stu-id="831b6-132">INPUTS</span></span>

### <span data-ttu-id="831b6-133">ICustomProvidersIdentity （CustomProviders）的</span><span class="sxs-lookup"><span data-stu-id="831b6-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="831b6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="831b6-134">OUTPUTS</span></span>

### <span data-ttu-id="831b6-135">ICustomRpManifest （CustomProviders）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="831b6-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="831b6-136">筆記</span><span class="sxs-lookup"><span data-stu-id="831b6-136">NOTES</span></span>

<span data-ttu-id="831b6-137">別名</span><span class="sxs-lookup"><span data-stu-id="831b6-137">ALIASES</span></span>

<span data-ttu-id="831b6-138">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="831b6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="831b6-139">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="831b6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="831b6-140">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="831b6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="831b6-141">INPUTOBJECT <ICustomProvidersIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="831b6-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="831b6-142">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="831b6-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="831b6-143">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="831b6-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="831b6-144">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="831b6-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="831b6-145">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="831b6-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="831b6-146">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="831b6-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="831b6-147">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="831b6-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="831b6-148">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-000000000000) </span><span class="sxs-lookup"><span data-stu-id="831b6-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="831b6-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="831b6-149">RELATED LINKS</span></span>

