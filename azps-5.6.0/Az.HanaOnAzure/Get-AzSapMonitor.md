---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 0de9aa6dd623efa379a6123570e766d30c850ab8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917266"
---
# <span data-ttu-id="78da9-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="78da9-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="78da9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="78da9-102">SYNOPSIS</span></span>
<span data-ttu-id="78da9-103">為指定的訂閱、資源群組和資源名稱，獲取 SAP 監視器的屬性。</span><span class="sxs-lookup"><span data-stu-id="78da9-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="78da9-104">語法</span><span class="sxs-lookup"><span data-stu-id="78da9-104">SYNTAX</span></span>

### <span data-ttu-id="78da9-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="78da9-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="78da9-106">獲取</span><span class="sxs-lookup"><span data-stu-id="78da9-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="78da9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="78da9-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="78da9-108">描述</span><span class="sxs-lookup"><span data-stu-id="78da9-108">DESCRIPTION</span></span>
<span data-ttu-id="78da9-109">為指定的訂閱、資源群組和資源名稱，獲取 SAP 監視器的屬性。</span><span class="sxs-lookup"><span data-stu-id="78da9-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="78da9-110">例子</span><span class="sxs-lookup"><span data-stu-id="78da9-110">EXAMPLES</span></span>

### <span data-ttu-id="78da9-111">範例 1：取得訂閱下的所有 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="78da9-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="78da9-112">此命令在訂閱下會獲得 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="78da9-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="78da9-113">範例 2：根據名稱取得 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="78da9-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="78da9-114">此命令會按名稱獲得 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="78da9-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="78da9-115">範例 3：根據物件取得 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="78da9-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="78da9-116">此命令會按物件獲得 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="78da9-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="78da9-117">範例 4：根據管線取得 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="78da9-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="78da9-118">此命令會按管線獲得 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="78da9-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="78da9-119">參數</span><span class="sxs-lookup"><span data-stu-id="78da9-119">PARAMETERS</span></span>

### <span data-ttu-id="78da9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78da9-120">-DefaultProfile</span></span>
<span data-ttu-id="78da9-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="78da9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78da9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78da9-122">-InputObject</span></span>
<span data-ttu-id="78da9-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="78da9-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78da9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="78da9-124">-Name</span></span>
<span data-ttu-id="78da9-125">SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="78da9-125">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78da9-126">-ResourceGroupName</span></span>
<span data-ttu-id="78da9-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78da9-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da9-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78da9-128">-SubscriptionId</span></span>
<span data-ttu-id="78da9-129">可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="78da9-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="78da9-130">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="78da9-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78da9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78da9-131">CommonParameters</span></span>
<span data-ttu-id="78da9-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="78da9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78da9-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78da9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78da9-134">輸入</span><span class="sxs-lookup"><span data-stu-id="78da9-134">INPUTS</span></span>

### <span data-ttu-id="78da9-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="78da9-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="78da9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="78da9-136">OUTPUTS</span></span>

### <span data-ttu-id="78da9-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="78da9-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="78da9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="78da9-138">NOTES</span></span>

<span data-ttu-id="78da9-139">別名</span><span class="sxs-lookup"><span data-stu-id="78da9-139">ALIASES</span></span>

<span data-ttu-id="78da9-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="78da9-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="78da9-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="78da9-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="78da9-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="78da9-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="78da9-143">INPUTOBJECT： <IHanaOnAzureIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="78da9-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="78da9-144">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="78da9-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="78da9-145">`[Location <String>]`：已刪除的儲存庫位置。</span><span class="sxs-lookup"><span data-stu-id="78da9-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="78da9-146">`[OperationKind <AccessPolicyUpdateKind?>]`：作業名稱</span><span class="sxs-lookup"><span data-stu-id="78da9-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="78da9-147">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="78da9-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="78da9-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78da9-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="78da9-149">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="78da9-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="78da9-150">`[SapMonitorName <String>]`：SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="78da9-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="78da9-151">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="78da9-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="78da9-152">受管理身分驗證擴充的父資源。</span><span class="sxs-lookup"><span data-stu-id="78da9-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="78da9-153">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="78da9-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="78da9-154">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="78da9-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="78da9-155">`[VaultName <String>]`：儲存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="78da9-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="78da9-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="78da9-156">RELATED LINKS</span></span>

