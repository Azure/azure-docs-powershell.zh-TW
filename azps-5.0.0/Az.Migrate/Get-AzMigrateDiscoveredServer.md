---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 367d22f4cea200b59b63e3ddb39c1eaad749fc43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141521"
---
# <span data-ttu-id="a03b5-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="a03b5-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="a03b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a03b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a03b5-103">在遷移專案中取得所有已探索的伺服器。</span><span class="sxs-lookup"><span data-stu-id="a03b5-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="a03b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="a03b5-104">SYNTAX</span></span>

### <span data-ttu-id="a03b5-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="a03b5-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a03b5-106">獲取</span><span class="sxs-lookup"><span data-stu-id="a03b5-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a03b5-107">GetInSite</span><span class="sxs-lookup"><span data-stu-id="a03b5-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a03b5-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="a03b5-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a03b5-109">說明</span><span class="sxs-lookup"><span data-stu-id="a03b5-109">DESCRIPTION</span></span>
<span data-ttu-id="a03b5-110">[取得 Azure 遷移伺服器] commandlet 會取得遷移專案中的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="a03b5-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="a03b5-111">示例</span><span class="sxs-lookup"><span data-stu-id="a03b5-111">EXAMPLES</span></span>

### <span data-ttu-id="a03b5-112">範例1：清單</span><span class="sxs-lookup"><span data-stu-id="a03b5-112">Example 1: List</span></span>
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

<span data-ttu-id="a03b5-113">取得遷移專案中的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="a03b5-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="a03b5-114">範例2：取得</span><span class="sxs-lookup"><span data-stu-id="a03b5-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="a03b5-115">透過名稱在 [遷移專案] 中取得伺服器。</span><span class="sxs-lookup"><span data-stu-id="a03b5-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="a03b5-116">[名稱] 是伺服器的唯一 paramenter。</span><span class="sxs-lookup"><span data-stu-id="a03b5-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="a03b5-117">範例3：裝置中的清單</span><span class="sxs-lookup"><span data-stu-id="a03b5-117">Example 3: List in an appliance</span></span>
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

<span data-ttu-id="a03b5-118">列出專案中裝置的所有伺服器。</span><span class="sxs-lookup"><span data-stu-id="a03b5-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="a03b5-119">範例4：取得裝置</span><span class="sxs-lookup"><span data-stu-id="a03b5-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="a03b5-120">在專案中取得裝置的伺服器。</span><span class="sxs-lookup"><span data-stu-id="a03b5-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="a03b5-121">[名稱] 是伺服器的唯一 paramenter。</span><span class="sxs-lookup"><span data-stu-id="a03b5-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="a03b5-122">範例5：依顯示名稱列出及篩選</span><span class="sxs-lookup"><span data-stu-id="a03b5-122">Example 5: List and filter by display name</span></span>
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

<span data-ttu-id="a03b5-123">[遷移專案] 中的 [清單伺服器] 與 [顯示名稱] 的篩選回應。</span><span class="sxs-lookup"><span data-stu-id="a03b5-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="a03b5-124">範例6：裝置中的清單並依顯示名稱篩選</span><span class="sxs-lookup"><span data-stu-id="a03b5-124">Example 6: List in an appliance and filter by display name</span></span>
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

<span data-ttu-id="a03b5-125">[遷移專案] 中裝置的 [清單伺服器] 和 [顯示名稱的篩選回應]。</span><span class="sxs-lookup"><span data-stu-id="a03b5-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="a03b5-126">參數</span><span class="sxs-lookup"><span data-stu-id="a03b5-126">PARAMETERS</span></span>

### <span data-ttu-id="a03b5-127">-ApplianceName</span><span class="sxs-lookup"><span data-stu-id="a03b5-127">-ApplianceName</span></span>
<span data-ttu-id="a03b5-128">指定裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="a03b5-128">Specifies the appliance name.</span></span>
<span data-ttu-id="a03b5-129">此內部對應至網站。</span><span class="sxs-lookup"><span data-stu-id="a03b5-129">This internally maps to a site.</span></span>

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

### <span data-ttu-id="a03b5-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a03b5-130">-DisplayName</span></span>
<span data-ttu-id="a03b5-131">指定 VMware 電腦顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a03b5-131">Specifies the VMware machine display name.</span></span>

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

### <span data-ttu-id="a03b5-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="a03b5-132">-Name</span></span>
<span data-ttu-id="a03b5-133">指定 VMware 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a03b5-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="a03b5-134">這是內部名稱。</span><span class="sxs-lookup"><span data-stu-id="a03b5-134">This is an internal Name.</span></span>
<span data-ttu-id="a03b5-135">針對使用者，請使用 [顯示名稱]。</span><span class="sxs-lookup"><span data-stu-id="a03b5-135">For users, use display name.</span></span>

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

### <span data-ttu-id="a03b5-136">-專案名稱</span><span class="sxs-lookup"><span data-stu-id="a03b5-136">-ProjectName</span></span>
<span data-ttu-id="a03b5-137">指定 [遷移專案名稱]。</span><span class="sxs-lookup"><span data-stu-id="a03b5-137">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="a03b5-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a03b5-138">-ResourceGroupName</span></span>
<span data-ttu-id="a03b5-139">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a03b5-139">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="a03b5-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a03b5-140">-SubscriptionId</span></span>
<span data-ttu-id="a03b5-141">指定訂閱 id。</span><span class="sxs-lookup"><span data-stu-id="a03b5-141">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="a03b5-142">-確認</span><span class="sxs-lookup"><span data-stu-id="a03b5-142">-Confirm</span></span>
<span data-ttu-id="a03b5-143">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a03b5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a03b5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a03b5-144">-WhatIf</span></span>
<span data-ttu-id="a03b5-145">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a03b5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a03b5-146">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a03b5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a03b5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03b5-147">CommonParameters</span></span>
<span data-ttu-id="a03b5-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a03b5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03b5-149">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a03b5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03b5-150">輸入</span><span class="sxs-lookup"><span data-stu-id="a03b5-150">INPUTS</span></span>

## <span data-ttu-id="a03b5-151">輸出</span><span class="sxs-lookup"><span data-stu-id="a03b5-151">OUTPUTS</span></span>

### <span data-ttu-id="a03b5-152">IVMwareMachine 中的 Api202001 （）。</span><span class="sxs-lookup"><span data-stu-id="a03b5-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="a03b5-153">筆記</span><span class="sxs-lookup"><span data-stu-id="a03b5-153">NOTES</span></span>

<span data-ttu-id="a03b5-154">別名</span><span class="sxs-lookup"><span data-stu-id="a03b5-154">ALIASES</span></span>

## <span data-ttu-id="a03b5-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="a03b5-155">RELATED LINKS</span></span>

