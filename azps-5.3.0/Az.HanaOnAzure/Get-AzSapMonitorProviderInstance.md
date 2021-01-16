---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289120"
---
# <span data-ttu-id="85ad7-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="85ad7-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="85ad7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="85ad7-103">針對指定的訂閱、資源群組、SapMonitor 名稱和資源名稱，取得提供者實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="85ad7-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="85ad7-104">句法</span><span class="sxs-lookup"><span data-stu-id="85ad7-104">SYNTAX</span></span>

### <span data-ttu-id="85ad7-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="85ad7-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="85ad7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="85ad7-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="85ad7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85ad7-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="85ad7-108">說明</span><span class="sxs-lookup"><span data-stu-id="85ad7-108">DESCRIPTION</span></span>
<span data-ttu-id="85ad7-109">針對指定的訂閱、資源群組、SapMonitor 名稱和資源名稱，取得提供者實例的屬性。</span><span class="sxs-lookup"><span data-stu-id="85ad7-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="85ad7-110">示例</span><span class="sxs-lookup"><span data-stu-id="85ad7-110">EXAMPLES</span></span>

### <span data-ttu-id="85ad7-111">範例1：在 SAP 監視器中取得所有實例</span><span class="sxs-lookup"><span data-stu-id="85ad7-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="85ad7-112">這個命令會在 SAP monitor 下取得所有實例。</span><span class="sxs-lookup"><span data-stu-id="85ad7-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="85ad7-113">範例2：依名稱取得 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="85ad7-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="85ad7-114">這個命令會透過名稱取得 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="85ad7-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="85ad7-115">範例3：透過物件取得 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="85ad7-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="85ad7-116">這個命令會透過物件取得 SAP monitor 的實例。</span><span class="sxs-lookup"><span data-stu-id="85ad7-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="85ad7-117">範例4：透過管道取得 SAP 監視器的實例</span><span class="sxs-lookup"><span data-stu-id="85ad7-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="85ad7-118">這個命令會透過管道取得 SAP 監視器的實例。</span><span class="sxs-lookup"><span data-stu-id="85ad7-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="85ad7-119">參數</span><span class="sxs-lookup"><span data-stu-id="85ad7-119">PARAMETERS</span></span>

### <span data-ttu-id="85ad7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ad7-120">-DefaultProfile</span></span>
<span data-ttu-id="85ad7-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85ad7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85ad7-122">-InputObject</span></span>
<span data-ttu-id="85ad7-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="85ad7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="85ad7-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="85ad7-124">-Name</span></span>
<span data-ttu-id="85ad7-125">提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-125">Name of the provider instance.</span></span>

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

### <span data-ttu-id="85ad7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ad7-126">-ResourceGroupName</span></span>
<span data-ttu-id="85ad7-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="85ad7-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="85ad7-128">-SapMonitorName</span></span>
<span data-ttu-id="85ad7-129">SAP 監視資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="85ad7-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85ad7-130">-SubscriptionId</span></span>
<span data-ttu-id="85ad7-131">訂閱識別碼，可唯一識別 Microsoft Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="85ad7-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="85ad7-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="85ad7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ad7-133">CommonParameters</span></span>
<span data-ttu-id="85ad7-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85ad7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ad7-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="85ad7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ad7-136">輸入</span><span class="sxs-lookup"><span data-stu-id="85ad7-136">INPUTS</span></span>

### <span data-ttu-id="85ad7-137">IHanaOnAzureIdentity （HanaOnAzure）的</span><span class="sxs-lookup"><span data-stu-id="85ad7-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="85ad7-138">輸出</span><span class="sxs-lookup"><span data-stu-id="85ad7-138">OUTPUTS</span></span>

### <span data-ttu-id="85ad7-139">IProviderInstance （HanaOnAzure）。 Api20200207Preview。</span><span class="sxs-lookup"><span data-stu-id="85ad7-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="85ad7-140">筆記</span><span class="sxs-lookup"><span data-stu-id="85ad7-140">NOTES</span></span>

<span data-ttu-id="85ad7-141">別名</span><span class="sxs-lookup"><span data-stu-id="85ad7-141">ALIASES</span></span>

<span data-ttu-id="85ad7-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="85ad7-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="85ad7-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="85ad7-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85ad7-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="85ad7-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="85ad7-145">INPUTOBJECT <IHanaOnAzureIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="85ad7-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85ad7-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="85ad7-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85ad7-147">`[Location <String>]`：已刪除的保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="85ad7-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="85ad7-148">`[OperationKind <AccessPolicyUpdateKind?>]`：操作的名稱</span><span class="sxs-lookup"><span data-stu-id="85ad7-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="85ad7-149">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="85ad7-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="85ad7-151">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="85ad7-152">`[SapMonitorName <String>]`： SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ad7-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="85ad7-153">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="85ad7-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="85ad7-154">受管理的身分識別的父資源。</span><span class="sxs-lookup"><span data-stu-id="85ad7-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="85ad7-155">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="85ad7-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="85ad7-156">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="85ad7-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="85ad7-157">`[VaultName <String>]`：保存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="85ad7-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="85ad7-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="85ad7-158">RELATED LINKS</span></span>

