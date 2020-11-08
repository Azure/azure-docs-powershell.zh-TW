---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitor.md
ms.openlocfilehash: 1ec82e745c7f6521a62db80ca109078bb1681172
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136793"
---
# <span data-ttu-id="f263b-101">Get-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="f263b-101">Get-AzSapMonitor</span></span>

## <span data-ttu-id="f263b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f263b-102">SYNOPSIS</span></span>
<span data-ttu-id="f263b-103">針對指定的訂閱、資源群組和資源名稱，取得 SAP 監視器的屬性。</span><span class="sxs-lookup"><span data-stu-id="f263b-103">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="f263b-104">句法</span><span class="sxs-lookup"><span data-stu-id="f263b-104">SYNTAX</span></span>

### <span data-ttu-id="f263b-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="f263b-105">List (Default)</span></span>
```
Get-AzSapMonitor [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f263b-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f263b-106">Get</span></span>
```
Get-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f263b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f263b-107">GetViaIdentity</span></span>
```
Get-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f263b-108">說明</span><span class="sxs-lookup"><span data-stu-id="f263b-108">DESCRIPTION</span></span>
<span data-ttu-id="f263b-109">針對指定的訂閱、資源群組和資源名稱，取得 SAP 監視器的屬性。</span><span class="sxs-lookup"><span data-stu-id="f263b-109">Gets properties of a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="f263b-110">示例</span><span class="sxs-lookup"><span data-stu-id="f263b-110">EXAMPLES</span></span>

### <span data-ttu-id="f263b-111">範例1：取得訂閱中的所有 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="f263b-111">Example 1: Get all SAP monitors under a subscription</span></span>
```powershell
PS C:\> Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="f263b-112">這個命令會在訂閱下取得 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="f263b-112">This command gets SAP monitors under a subscription.</span></span>

### <span data-ttu-id="f263b-113">範例2：依名稱取得 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="f263b-113">Example 2: Get a SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="f263b-114">這個命令會透過名稱取得 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="f263b-114">This command gets a SAP monitor by name.</span></span>

### <span data-ttu-id="f263b-115">範例3：透過物件取得 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="f263b-115">Example 3: Get a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01
PS C:\> Get-AzSapMonitor -InputObject $sap

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="f263b-116">這個命令會透過物件取得 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="f263b-116">This command gets a SAP monitor by object.</span></span>

### <span data-ttu-id="f263b-117">範例4：透過管線取得 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="f263b-117">Example 4: Get a SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id='/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01'} | Get-AzSapMonitor

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="f263b-118">這個命令會透過管線取得 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="f263b-118">This command gets a SAP monitor by pipeline.</span></span>

## <span data-ttu-id="f263b-119">參數</span><span class="sxs-lookup"><span data-stu-id="f263b-119">PARAMETERS</span></span>

### <span data-ttu-id="f263b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f263b-120">-DefaultProfile</span></span>
<span data-ttu-id="f263b-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f263b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f263b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f263b-122">-InputObject</span></span>
<span data-ttu-id="f263b-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f263b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f263b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f263b-124">-Name</span></span>
<span data-ttu-id="f263b-125">SAP 監視資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f263b-125">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="f263b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f263b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f263b-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f263b-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="f263b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f263b-128">-SubscriptionId</span></span>
<span data-ttu-id="f263b-129">訂閱識別碼，可唯一識別 Microsoft Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="f263b-129">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f263b-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f263b-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f263b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f263b-131">CommonParameters</span></span>
<span data-ttu-id="f263b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f263b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f263b-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f263b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f263b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f263b-134">INPUTS</span></span>

### <span data-ttu-id="f263b-135">IHanaOnAzureIdentity （HanaOnAzure）的</span><span class="sxs-lookup"><span data-stu-id="f263b-135">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="f263b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f263b-136">OUTPUTS</span></span>

### <span data-ttu-id="f263b-137">ISapMonitor （HanaOnAzure）。 Api20200207Preview。</span><span class="sxs-lookup"><span data-stu-id="f263b-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="f263b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f263b-138">NOTES</span></span>

<span data-ttu-id="f263b-139">別名</span><span class="sxs-lookup"><span data-stu-id="f263b-139">ALIASES</span></span>

<span data-ttu-id="f263b-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f263b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f263b-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f263b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f263b-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f263b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f263b-143">INPUTOBJECT <IHanaOnAzureIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f263b-143">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f263b-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f263b-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f263b-145">`[Location <String>]`：已刪除的保存庫的位置。</span><span class="sxs-lookup"><span data-stu-id="f263b-145">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="f263b-146">`[OperationKind <AccessPolicyUpdateKind?>]`：操作的名稱</span><span class="sxs-lookup"><span data-stu-id="f263b-146">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="f263b-147">`[ProviderInstanceName <String>]`：提供者實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="f263b-147">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="f263b-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f263b-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f263b-149">`[ResourceName <String>]`：身分識別資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f263b-149">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="f263b-150">`[SapMonitorName <String>]`： SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f263b-150">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="f263b-151">`[Scope <String>]`：資源的資源提供者範圍。</span><span class="sxs-lookup"><span data-stu-id="f263b-151">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="f263b-152">受管理的身分識別的父資源。</span><span class="sxs-lookup"><span data-stu-id="f263b-152">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="f263b-153">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f263b-153">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f263b-154">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f263b-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f263b-155">`[VaultName <String>]`：保存庫的名稱</span><span class="sxs-lookup"><span data-stu-id="f263b-155">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="f263b-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="f263b-156">RELATED LINKS</span></span>

