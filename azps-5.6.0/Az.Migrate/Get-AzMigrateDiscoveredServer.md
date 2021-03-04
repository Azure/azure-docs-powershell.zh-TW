---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 79a61ea316247fe3d76f5ad0b202d30037cb839c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909662"
---
# <span data-ttu-id="f32a1-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="f32a1-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="f32a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f32a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f32a1-103">在遷移專案中取得所有發現的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f32a1-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="f32a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="f32a1-104">SYNTAX</span></span>

### <span data-ttu-id="f32a1-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="f32a1-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f32a1-106">獲取</span><span class="sxs-lookup"><span data-stu-id="f32a1-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f32a1-107">GetInSite</span><span class="sxs-lookup"><span data-stu-id="f32a1-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f32a1-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="f32a1-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f32a1-109">描述</span><span class="sxs-lookup"><span data-stu-id="f32a1-109">DESCRIPTION</span></span>
<span data-ttu-id="f32a1-110">取得 Azure Migrate Server Commandlet 會抓取一個遷移專案中的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="f32a1-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="f32a1-111">例子</span><span class="sxs-lookup"><span data-stu-id="f32a1-111">EXAMPLES</span></span>

### <span data-ttu-id="f32a1-112">範例 1：清單</span><span class="sxs-lookup"><span data-stu-id="f32a1-112">Example 1: List</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="f32a1-113">在遷移專案中取得所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="f32a1-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="f32a1-114">範例 2：取得</span><span class="sxs-lookup"><span data-stu-id="f32a1-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="f32a1-115">以名稱在專案遷移中取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="f32a1-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="f32a1-116">名稱是伺服器的唯一參數。</span><span class="sxs-lookup"><span data-stu-id="f32a1-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="f32a1-117">範例 3：設備中的清單</span><span class="sxs-lookup"><span data-stu-id="f32a1-117">Example 3: List in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="f32a1-118">列出專案中設備的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="f32a1-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="f32a1-119">範例 4：使用設備</span><span class="sxs-lookup"><span data-stu-id="f32a1-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="f32a1-120">取得專案中設備的伺服器。</span><span class="sxs-lookup"><span data-stu-id="f32a1-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="f32a1-121">名稱是伺服器的唯一參數。</span><span class="sxs-lookup"><span data-stu-id="f32a1-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="f32a1-122">範例 5：根據顯示名稱列出和篩選</span><span class="sxs-lookup"><span data-stu-id="f32a1-122">Example 5: List and filter by display name</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="f32a1-123">在專案遷移中列出伺服器，並篩選具有顯示名稱的回應。</span><span class="sxs-lookup"><span data-stu-id="f32a1-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="f32a1-124">範例 6：裝置中的清單，並按顯示名稱篩選</span><span class="sxs-lookup"><span data-stu-id="f32a1-124">Example 6: List in an appliance and filter by display name</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -ApplianceName BBVMwareAVS -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines
Contoso-DataTier3             10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_500986e5-7720-471e-11d7-d4e8ae9edc45 Microsoft.OffAzure/VMwareSites/machines
```

<span data-ttu-id="f32a1-125">在專案遷移中列出設備的清單伺服器，並篩選具有顯示名稱的回應。</span><span class="sxs-lookup"><span data-stu-id="f32a1-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="f32a1-126">參數</span><span class="sxs-lookup"><span data-stu-id="f32a1-126">PARAMETERS</span></span>

### <span data-ttu-id="f32a1-127">-設備名稱</span><span class="sxs-lookup"><span data-stu-id="f32a1-127">-ApplianceName</span></span>
<span data-ttu-id="f32a1-128">指定設備名稱。</span><span class="sxs-lookup"><span data-stu-id="f32a1-128">Specifies the appliance name.</span></span>
<span data-ttu-id="f32a1-129">這會在內部與網站進行連結。</span><span class="sxs-lookup"><span data-stu-id="f32a1-129">This internally maps to a site.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInSite, ListInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32a1-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f32a1-130">-DisplayName</span></span>
<span data-ttu-id="f32a1-131">指定 V1 電腦顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f32a1-131">Specifies the VMware machine display name.</span></span>

```yaml
Type: System.String
Parameter Sets: List, ListInSite
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32a1-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="f32a1-132">-Name</span></span>
<span data-ttu-id="f32a1-133">指定 V1 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f32a1-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="f32a1-134">這是內部名稱。</span><span class="sxs-lookup"><span data-stu-id="f32a1-134">This is an internal Name.</span></span>
<span data-ttu-id="f32a1-135">對於使用者，請使用顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f32a1-135">For users, use display name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32a1-136">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="f32a1-136">-ProjectName</span></span>
<span data-ttu-id="f32a1-137">指定要遷移的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="f32a1-137">Specifies the migrate project name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32a1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f32a1-138">-ResourceGroupName</span></span>
<span data-ttu-id="f32a1-139">指定資源組名。</span><span class="sxs-lookup"><span data-stu-id="f32a1-139">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32a1-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f32a1-140">-SubscriptionId</span></span>
<span data-ttu-id="f32a1-141">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f32a1-141">Specifies the subscription id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32a1-142">-確認</span><span class="sxs-lookup"><span data-stu-id="f32a1-142">-Confirm</span></span>
<span data-ttu-id="f32a1-143">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f32a1-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32a1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f32a1-144">-WhatIf</span></span>
<span data-ttu-id="f32a1-145">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f32a1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f32a1-146">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f32a1-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32a1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32a1-147">CommonParameters</span></span>
<span data-ttu-id="f32a1-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f32a1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32a1-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f32a1-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32a1-150">輸入</span><span class="sxs-lookup"><span data-stu-id="f32a1-150">INPUTS</span></span>

## <span data-ttu-id="f32a1-151">輸出</span><span class="sxs-lookup"><span data-stu-id="f32a1-151">OUTPUTS</span></span>

### <span data-ttu-id="f32a1-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVVtMachine</span><span class="sxs-lookup"><span data-stu-id="f32a1-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="f32a1-153">筆記</span><span class="sxs-lookup"><span data-stu-id="f32a1-153">NOTES</span></span>

<span data-ttu-id="f32a1-154">別名</span><span class="sxs-lookup"><span data-stu-id="f32a1-154">ALIASES</span></span>

## <span data-ttu-id="f32a1-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="f32a1-155">RELATED LINKS</span></span>

