---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: f7c36ca53b00c0fc99e5afc6e6ba74f4cff62afb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914133"
---
# <span data-ttu-id="4f09f-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="4f09f-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="4f09f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4f09f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f09f-103">取得關聯。</span><span class="sxs-lookup"><span data-stu-id="4f09f-103">Get an association.</span></span>

## <span data-ttu-id="4f09f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4f09f-104">SYNTAX</span></span>

### <span data-ttu-id="4f09f-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="4f09f-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4f09f-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4f09f-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f09f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f09f-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f09f-108">描述</span><span class="sxs-lookup"><span data-stu-id="4f09f-108">DESCRIPTION</span></span>
<span data-ttu-id="4f09f-109">取得關聯。</span><span class="sxs-lookup"><span data-stu-id="4f09f-109">Get an association.</span></span>

## <span data-ttu-id="4f09f-110">例子</span><span class="sxs-lookup"><span data-stu-id="4f09f-110">EXAMPLES</span></span>

### <span data-ttu-id="4f09f-111">範例 1：列出自訂提供者關聯</span><span class="sxs-lookup"><span data-stu-id="4f09f-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="4f09f-112">列出給定範圍的所有自訂提供者關聯。</span><span class="sxs-lookup"><span data-stu-id="4f09f-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="4f09f-113">範例 2：取得關聯</span><span class="sxs-lookup"><span data-stu-id="4f09f-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="4f09f-114">取得單一 CustomProvider 關聯的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="4f09f-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="4f09f-115">參數</span><span class="sxs-lookup"><span data-stu-id="4f09f-115">PARAMETERS</span></span>

### <span data-ttu-id="4f09f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f09f-116">-DefaultProfile</span></span>
<span data-ttu-id="4f09f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f09f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f09f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f09f-118">-InputObject</span></span>
<span data-ttu-id="4f09f-119">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4f09f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4f09f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f09f-120">-Name</span></span>
<span data-ttu-id="4f09f-121">關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f09f-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f09f-122">-範圍</span><span class="sxs-lookup"><span data-stu-id="4f09f-122">-Scope</span></span>
<span data-ttu-id="4f09f-123">關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="4f09f-123">The scope of the association.</span></span>

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

### <span data-ttu-id="4f09f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f09f-124">CommonParameters</span></span>
<span data-ttu-id="4f09f-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4f09f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f09f-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f09f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f09f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4f09f-127">INPUTS</span></span>

### <span data-ttu-id="4f09f-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="4f09f-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="4f09f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4f09f-129">OUTPUTS</span></span>

### <span data-ttu-id="4f09f-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="4f09f-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="4f09f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4f09f-131">NOTES</span></span>

<span data-ttu-id="4f09f-132">別名</span><span class="sxs-lookup"><span data-stu-id="4f09f-132">ALIASES</span></span>

<span data-ttu-id="4f09f-133">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4f09f-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f09f-134">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4f09f-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f09f-135">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4f09f-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f09f-136">INPUTOBJECT： <ICustomProvidersIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4f09f-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f09f-137">`[AssociationName <String>]`：關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f09f-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="4f09f-138">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4f09f-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f09f-139">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f09f-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4f09f-140">`[ResourceProviderName <String>]`：資源提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f09f-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="4f09f-141">`[Scope <String>]`：關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="4f09f-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="4f09f-142">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f09f-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="4f09f-143">這是 GUID 格式的字串 (例如 00000000-0000-0000-0000-00000000000000000000000000000000000000000000000000000) </span><span class="sxs-lookup"><span data-stu-id="4f09f-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="4f09f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f09f-144">RELATED LINKS</span></span>

