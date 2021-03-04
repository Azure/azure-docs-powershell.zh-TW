---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917070"
---
# <span data-ttu-id="e3e92-101">Get-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="e3e92-101">Get-AzConfluentOrganization</span></span>

## <span data-ttu-id="e3e92-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3e92-102">SYNOPSIS</span></span>
<span data-ttu-id="e3e92-103">取得特定組織資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3e92-103">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="e3e92-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3e92-104">SYNTAX</span></span>

### <span data-ttu-id="e3e92-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="e3e92-105">List (Default)</span></span>
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3e92-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e3e92-106">Get</span></span>
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3e92-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3e92-107">GetViaIdentity</span></span>
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3e92-108">清單1</span><span class="sxs-lookup"><span data-stu-id="e3e92-108">List1</span></span>
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e3e92-109">描述</span><span class="sxs-lookup"><span data-stu-id="e3e92-109">DESCRIPTION</span></span>
<span data-ttu-id="e3e92-110">取得特定組織資源的屬性。</span><span class="sxs-lookup"><span data-stu-id="e3e92-110">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="e3e92-111">例子</span><span class="sxs-lookup"><span data-stu-id="e3e92-111">EXAMPLES</span></span>

### <span data-ttu-id="e3e92-112">範例 1：在訂閱下列出所有不必要的組織</span><span class="sxs-lookup"><span data-stu-id="e3e92-112">Example 1: List all confluent organizations under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

<span data-ttu-id="e3e92-113">此命令會列出訂閱下所有不必要的組織。</span><span class="sxs-lookup"><span data-stu-id="e3e92-113">This command lists all confluent organizations under a subscription.</span></span>

### <span data-ttu-id="e3e92-114">範例 2：在資源群組下列出所有不必要的組織</span><span class="sxs-lookup"><span data-stu-id="e3e92-114">Example 2: List all confluent organizations under a resource group</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

<span data-ttu-id="e3e92-115">此命令會列出資源群組下所有不必要的組織。</span><span class="sxs-lookup"><span data-stu-id="e3e92-115">This command lists all confluent organizations under a resource group.</span></span>

### <span data-ttu-id="e3e92-116">範例 3：根據名稱取得一個多餘的組織</span><span class="sxs-lookup"><span data-stu-id="e3e92-116">Example 3: Get a confluent organization by name</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

<span data-ttu-id="e3e92-117">此命令會按名稱得到一個不必要的組織。</span><span class="sxs-lookup"><span data-stu-id="e3e92-117">This command gets a confluent organization by name.</span></span>

### <span data-ttu-id="e3e92-118">範例 4：根據管線取得一個匯流組織</span><span class="sxs-lookup"><span data-stu-id="e3e92-118">Example 4: Get a confluent organization by pipeline</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="e3e92-119">此命令會根據管線得到一個不必要的組織。</span><span class="sxs-lookup"><span data-stu-id="e3e92-119">This command gets a confluent organization by pipeline.</span></span>

## <span data-ttu-id="e3e92-120">參數</span><span class="sxs-lookup"><span data-stu-id="e3e92-120">PARAMETERS</span></span>

### <span data-ttu-id="e3e92-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3e92-121">-DefaultProfile</span></span>
<span data-ttu-id="e3e92-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3e92-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3e92-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3e92-123">-InputObject</span></span>
<span data-ttu-id="e3e92-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e3e92-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3e92-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3e92-125">-Name</span></span>
<span data-ttu-id="e3e92-126">組織資源名稱</span><span class="sxs-lookup"><span data-stu-id="e3e92-126">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3e92-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3e92-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3e92-128">資源組名</span><span class="sxs-lookup"><span data-stu-id="e3e92-128">Resource group name</span></span>

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

### <span data-ttu-id="e3e92-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3e92-129">-SubscriptionId</span></span>
<span data-ttu-id="e3e92-130">Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="e3e92-130">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="e3e92-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3e92-131">CommonParameters</span></span>
<span data-ttu-id="e3e92-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3e92-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3e92-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3e92-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3e92-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e3e92-134">INPUTS</span></span>

### <span data-ttu-id="e3e92-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="e3e92-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="e3e92-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e3e92-136">OUTPUTS</span></span>

### <span data-ttu-id="e3e92-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="e3e92-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="e3e92-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e3e92-138">NOTES</span></span>

<span data-ttu-id="e3e92-139">別名</span><span class="sxs-lookup"><span data-stu-id="e3e92-139">ALIASES</span></span>

<span data-ttu-id="e3e92-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="e3e92-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3e92-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e3e92-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3e92-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e3e92-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3e92-143">INPUTOBJECT： <IConfluentIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e3e92-143">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3e92-144">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="e3e92-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3e92-145">`[OrganizationName <String>]`：組織資源名稱</span><span class="sxs-lookup"><span data-stu-id="e3e92-145">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="e3e92-146">`[ResourceGroupName <String>]`：資源組名</span><span class="sxs-lookup"><span data-stu-id="e3e92-146">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="e3e92-147">`[SubscriptionId <String>]`：Microsoft Azure 訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="e3e92-147">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="e3e92-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3e92-148">RELATED LINKS</span></span>

