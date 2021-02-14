---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/get-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Get-AzADDomainService.md
ms.openlocfilehash: ec52bea37eed3bb785da80beb8dfba02d0a426cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127318"
---
# <span data-ttu-id="48045-101">Get-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-101">Get-AzADDomainService</span></span>

## <span data-ttu-id="48045-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48045-102">SYNOPSIS</span></span>
<span data-ttu-id="48045-103">[取得網域服務] 作業會檢索網域服務的 json 表示。</span><span class="sxs-lookup"><span data-stu-id="48045-103">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="48045-104">句法</span><span class="sxs-lookup"><span data-stu-id="48045-104">SYNTAX</span></span>

### <span data-ttu-id="48045-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="48045-105">List (Default)</span></span>
```
Get-AzADDomainService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48045-106">獲取</span><span class="sxs-lookup"><span data-stu-id="48045-106">Get</span></span>
```
Get-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="48045-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48045-107">GetViaIdentity</span></span>
```
Get-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="48045-108">List1</span><span class="sxs-lookup"><span data-stu-id="48045-108">List1</span></span>
```
Get-AzADDomainService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="48045-109">說明</span><span class="sxs-lookup"><span data-stu-id="48045-109">DESCRIPTION</span></span>
<span data-ttu-id="48045-110">[取得網域服務] 作業會檢索網域服務的 json 表示。</span><span class="sxs-lookup"><span data-stu-id="48045-110">The Get Domain Service operation retrieves a json representation of the Domain Service.</span></span>

## <span data-ttu-id="48045-111">示例</span><span class="sxs-lookup"><span data-stu-id="48045-111">EXAMPLES</span></span>

### <span data-ttu-id="48045-112">範例1：預設取得所有 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-112">Example 1: Get All ADDomainService By default</span></span>
```powershell
PS C:\> Get-AzADDomainService

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="48045-113">預設取得所有 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-113">Get All ADDomainService By default</span></span>

### <span data-ttu-id="48045-114">範例2：依 ResourceGroup 和名稱取得 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-114">Example 2: Get ADDomainService By ResourceGroup and name</span></span>
```powershell
PS C:\> Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="48045-115">依 ResourceGroup 和名稱取得 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-115">Get ADDomainService By ResourceGroup and name</span></span>

### <span data-ttu-id="48045-116">範例3：透過 ResourceGroup 取得所有 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-116">Example 3: Get all ADDomainService By ResourceGroup</span></span>
```powershell
PS C:\> Get-AzADDomainService -ResourceGroupName youriADdomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="48045-117">透過 ResourceGroup 取得所有 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-117">Get all ADDomainService By ResourceGroup</span></span>

### <span data-ttu-id="48045-118">範例4：透過 InputObject 取得 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-118">Example 4: Get ADDomainService By InputObject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
Get-AzADDomainService -InputObject $getAzAddomain

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="48045-119">透過 InputObject 取得 ADDomainService</span><span class="sxs-lookup"><span data-stu-id="48045-119">Get ADDomainService By InputObject</span></span>

## <span data-ttu-id="48045-120">參數</span><span class="sxs-lookup"><span data-stu-id="48045-120">PARAMETERS</span></span>

### <span data-ttu-id="48045-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48045-121">-DefaultProfile</span></span>
<span data-ttu-id="48045-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48045-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48045-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48045-123">-InputObject</span></span>
<span data-ttu-id="48045-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="48045-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48045-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="48045-125">-Name</span></span>
<span data-ttu-id="48045-126">網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="48045-126">The name of the domain service.</span></span>

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

### <span data-ttu-id="48045-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48045-127">-ResourceGroupName</span></span>
<span data-ttu-id="48045-128">使用者訂閱中資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48045-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="48045-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="48045-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="48045-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48045-130">-SubscriptionId</span></span>
<span data-ttu-id="48045-131">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="48045-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="48045-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="48045-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="48045-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48045-133">CommonParameters</span></span>
<span data-ttu-id="48045-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48045-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48045-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48045-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48045-136">輸入</span><span class="sxs-lookup"><span data-stu-id="48045-136">INPUTS</span></span>

### <span data-ttu-id="48045-137">IAdDomainServicesIdentity （ADDomainServices）的</span><span class="sxs-lookup"><span data-stu-id="48045-137">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="48045-138">輸出</span><span class="sxs-lookup"><span data-stu-id="48045-138">OUTPUTS</span></span>

### <span data-ttu-id="48045-139">IDomainService （ADDomainServices）。 Api202001。</span><span class="sxs-lookup"><span data-stu-id="48045-139">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="48045-140">筆記</span><span class="sxs-lookup"><span data-stu-id="48045-140">NOTES</span></span>

<span data-ttu-id="48045-141">別名</span><span class="sxs-lookup"><span data-stu-id="48045-141">ALIASES</span></span>

<span data-ttu-id="48045-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="48045-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48045-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="48045-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48045-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="48045-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48045-145">INPUTOBJECT <IAdDomainServicesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="48045-145">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48045-146">`[DomainServiceName <String>]`：網域服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="48045-146">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="48045-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="48045-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48045-148">`[ResourceGroupName <String>]`：使用者訂閱中資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48045-148">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="48045-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="48045-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="48045-150">`[SubscriptionId <String>]`：取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="48045-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="48045-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="48045-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="48045-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="48045-152">RELATED LINKS</span></span>

