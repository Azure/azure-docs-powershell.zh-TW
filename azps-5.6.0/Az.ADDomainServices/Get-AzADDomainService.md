---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: 19ae45bf50c9ae54075e46a8db8fc66cc08e488a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913634"
---
# <span data-ttu-id="70b3e-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="70b3e-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="70b3e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="70b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="70b3e-103">Get Domain Service 作業會取得網域服務的 json 標記法。</span><span class="sxs-lookup"><span data-stu-id="70b3e-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="70b3e-104">語法</span><span class="sxs-lookup"><span data-stu-id="70b3e-104">SYNTAX</span></span>

### <span data-ttu-id="70b3e-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="70b3e-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70b3e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="70b3e-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="70b3e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="70b3e-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="70b3e-108">清單1</span><span class="sxs-lookup"><span data-stu-id="70b3e-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="70b3e-109">描述</span><span class="sxs-lookup"><span data-stu-id="70b3e-109">DESCRIPTION</span></span>
<span data-ttu-id="70b3e-110">Get Domain Service 作業會取得網域服務的 json 標記法。</span><span class="sxs-lookup"><span data-stu-id="70b3e-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="70b3e-111">例子</span><span class="sxs-lookup"><span data-stu-id="70b3e-111">EXAMPLES</span></span>

### <span data-ttu-id="70b3e-112">範例 1：根據預設取得 All ADDomainService</span><span class="sxs-lookup"><span data-stu-id="70b3e-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="70b3e-113">根據預設取得所有 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="70b3e-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="70b3e-114">範例 2：取得 ADDomainService By ResourceGroup 和名稱</span><span class="sxs-lookup"><span data-stu-id="70b3e-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="70b3e-115">取得 ADDomainService By ResourceGroup 和名稱</span><span class="sxs-lookup"><span data-stu-id="70b3e-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="70b3e-116">範例 3：取得所有 ADDomainService By ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="70b3e-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="70b3e-117">取得所有 ADDomainService By ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="70b3e-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="70b3e-118">範例 4：Get ADDomainService By InputObject</span><span class="sxs-lookup"><span data-stu-id="70b3e-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="70b3e-119">取得 ADDomainService By InputObject</span><span class="sxs-lookup"><span data-stu-id="70b3e-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="70b3e-120">參數</span><span class="sxs-lookup"><span data-stu-id="70b3e-120">PARAMETERS</span></span>

### <span data-ttu-id="70b3e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70b3e-121">-DefaultProfile</span></span>
<span data-ttu-id="70b3e-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="70b3e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70b3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70b3e-123">-InputObject</span></span>
<span data-ttu-id="70b3e-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="70b3e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70b3e-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="70b3e-125">-Name</span></span>
<span data-ttu-id="70b3e-126">網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="70b3e-126">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70b3e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70b3e-127">-ResourceGroupName</span></span>
<span data-ttu-id="70b3e-128">使用者訂閱中資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="70b3e-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="70b3e-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="70b3e-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70b3e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="70b3e-130">-SubscriptionId</span></span>
<span data-ttu-id="70b3e-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="70b3e-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="70b3e-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="70b3e-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="70b3e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70b3e-133">CommonParameters</span></span>
<span data-ttu-id="70b3e-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="70b3e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70b3e-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70b3e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70b3e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="70b3e-136">INPUTS</span></span>

### <span data-ttu-id="70b3e-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="70b3e-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="70b3e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="70b3e-138">OUTPUTS</span></span>

### <span data-ttu-id="70b3e-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="70b3e-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="70b3e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="70b3e-140">NOTES</span></span>

<span data-ttu-id="70b3e-141">別名</span><span class="sxs-lookup"><span data-stu-id="70b3e-141">ALIASES</span></span>

<span data-ttu-id="70b3e-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="70b3e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="70b3e-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="70b3e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="70b3e-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="70b3e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="70b3e-145">INPUTOBJECT： <IAdDomainServicesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="70b3e-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="70b3e-146">`[DomainServiceName <String>]`：網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="70b3e-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="70b3e-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="70b3e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="70b3e-148">`[ResourceGroupName <String>]`：使用者訂閱中的資源組名。</span><span class="sxs-lookup"><span data-stu-id="70b3e-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="70b3e-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="70b3e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="70b3e-150">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="70b3e-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="70b3e-151">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="70b3e-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="70b3e-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="70b3e-152">RELATED LINKS</span></span>

