---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 66f5a875f05b9c5d2fcdcc8a63eba9d149a9ba7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917265"
---
# <span data-ttu-id="4256e-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="4256e-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="4256e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4256e-102">SYNOPSIS</span></span>
<span data-ttu-id="4256e-103">為指定的訂閱、資源群組、SapMonitor 名稱和資源名稱，獲取提供者實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="4256e-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="4256e-104">語法</span><span class="sxs-lookup"><span data-stu-id="4256e-104">SYNTAX</span></span>

### <span data-ttu-id="4256e-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="4256e-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4256e-106">獲取</span><span class="sxs-lookup"><span data-stu-id="4256e-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4256e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4256e-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4256e-108">描述</span><span class="sxs-lookup"><span data-stu-id="4256e-108">DESCRIPTION</span></span>
<span data-ttu-id="4256e-109">為指定的訂閱、資源群組、SapMonitor 名稱和資源名稱，獲取提供者實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="4256e-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="4256e-110">例子</span><span class="sxs-lookup"><span data-stu-id="4256e-110">EXAMPLES</span></span>

### <span data-ttu-id="4256e-111">範例 1：在 SAP 監視器下取得所有實例</span><span class="sxs-lookup"><span data-stu-id="4256e-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4256e-112">此命令會獲得 SAP 監視器下的所有實例。</span><span class="sxs-lookup"><span data-stu-id="4256e-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="4256e-113">範例 2：根據名稱取得 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="4256e-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4256e-114">此命令會按名稱獲得 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="4256e-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="4256e-115">範例 3：根據物件取得 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="4256e-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4256e-116">此命令會按物件獲得 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="4256e-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="4256e-117">範例 4：根據管線取得 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="4256e-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="4256e-118">此命令會按管線獲得 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="4256e-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="4256e-119">參數</span><span class="sxs-lookup"><span data-stu-id="4256e-119">PARAMETERS</span></span>

### <span data-ttu-id="4256e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4256e-120">-DefaultProfile</span></span>
<span data-ttu-id="4256e-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4256e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4256e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4256e-122">-InputObject</span></span>
<span data-ttu-id="4256e-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4256e-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4256e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4256e-124">-Name</span></span>
<span data-ttu-id="4256e-125">提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="4256e-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4256e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4256e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4256e-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4256e-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="4256e-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="4256e-128">-SapMonitorName</span></span>
<span data-ttu-id="4256e-129">SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4256e-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="4256e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4256e-130">-SubscriptionId</span></span>
<span data-ttu-id="4256e-131">可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4256e-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4256e-132">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4256e-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4256e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4256e-133">CommonParameters</span></span>
<span data-ttu-id="4256e-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4256e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4256e-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4256e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4256e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4256e-136">INPUTS</span></span>

### <span data-ttu-id="4256e-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="4256e-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="4256e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4256e-138">OUTPUTS</span></span>

### <span data-ttu-id="4256e-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="4256e-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="4256e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4256e-140">NOTES</span></span>

<span data-ttu-id="4256e-141">別名</span><span class="sxs-lookup"><span data-stu-id="4256e-141">ALIASES</span></span>

<span data-ttu-id="4256e-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4256e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4256e-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4256e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4256e-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4256e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4256e-145">INPUTOBJECT： <IHanaOnAzureIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4256e-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4256e-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4256e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4256e-147">`[Location <String>]`：已刪除的儲存庫位置。</span><span class="sxs-lookup"><span data-stu-id="4256e-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="4256e-148">`[OperationKind <AccessPolicyUpdateKind?>]`：作業名稱</span><span class="sxs-lookup"><span data-stu-id="4256e-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="4256e-149">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="4256e-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="4256e-150">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4256e-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4256e-151">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4256e-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="4256e-152">`[SapMonitorName <String>]`：SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="4256e-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="4256e-153">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="4256e-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="4256e-154">受管理身分驗證擴充的父資源。</span><span class="sxs-lookup"><span data-stu-id="4256e-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="4256e-155">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4256e-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4256e-156">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4256e-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4256e-157">`[VaultName <String>]`：儲存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="4256e-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="4256e-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4256e-158">RELATED LINKS</span></span>

