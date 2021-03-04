---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: a13b0a936eeecd1d7a18b18bb8878b79225da030
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917262"
---
# <span data-ttu-id="26f0b-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="26f0b-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="26f0b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="26f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="26f0b-103">為指定的訂閱、資源群組和資源名稱建立 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="26f0b-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="26f0b-104">語法</span><span class="sxs-lookup"><span data-stu-id="26f0b-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="26f0b-105">描述</span><span class="sxs-lookup"><span data-stu-id="26f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="26f0b-106">為指定的訂閱、資源群組和資源名稱建立 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="26f0b-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="26f0b-107">例子</span><span class="sxs-lookup"><span data-stu-id="26f0b-107">EXAMPLES</span></span>

### <span data-ttu-id="26f0b-108">範例 1：新的 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="26f0b-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="26f0b-109">此命令會建立 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="26f0b-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="26f0b-110">參數</span><span class="sxs-lookup"><span data-stu-id="26f0b-110">PARAMETERS</span></span>

### <span data-ttu-id="26f0b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26f0b-111">-AsJob</span></span>
<span data-ttu-id="26f0b-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="26f0b-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f0b-113">-DefaultProfile</span></span>
<span data-ttu-id="26f0b-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="26f0b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f0b-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="26f0b-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="26f0b-116">指出是否要將分析傳送至 Microsoft 的值</span><span class="sxs-lookup"><span data-stu-id="26f0b-116">The value indicating whether to send analytics to Microsoft</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-117">-位置</span><span class="sxs-lookup"><span data-stu-id="26f0b-117">-Location</span></span>
<span data-ttu-id="26f0b-118">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="26f0b-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="26f0b-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="26f0b-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="26f0b-120">用來監控之記錄分析工作區的工作區識別碼</span><span class="sxs-lookup"><span data-stu-id="26f0b-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="26f0b-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="26f0b-122">用於監控之記錄分析工作區的 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="26f0b-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="26f0b-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="26f0b-124">用來監控之記錄分析工作區的共用金鑰</span><span class="sxs-lookup"><span data-stu-id="26f0b-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="26f0b-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="26f0b-126">將部署 SAP 監視器的子網。</span><span class="sxs-lookup"><span data-stu-id="26f0b-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="26f0b-127">它應該是同一個 HANA 資料庫子網。</span><span class="sxs-lookup"><span data-stu-id="26f0b-127">It should be the same subnet of HANA database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="26f0b-128">-Name</span></span>
<span data-ttu-id="26f0b-129">SAP 監視器資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="26f0b-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="26f0b-130">-NoWait</span></span>
<span data-ttu-id="26f0b-131">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="26f0b-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26f0b-132">-ResourceGroupName</span></span>
<span data-ttu-id="26f0b-133">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26f0b-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="26f0b-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26f0b-134">-SubscriptionId</span></span>
<span data-ttu-id="26f0b-135">可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="26f0b-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="26f0b-136">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="26f0b-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-137">-標記</span><span class="sxs-lookup"><span data-stu-id="26f0b-137">-Tag</span></span>
<span data-ttu-id="26f0b-138">資源標記。</span><span class="sxs-lookup"><span data-stu-id="26f0b-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26f0b-139">-確認</span><span class="sxs-lookup"><span data-stu-id="26f0b-139">-Confirm</span></span>
<span data-ttu-id="26f0b-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="26f0b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f0b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f0b-141">-WhatIf</span></span>
<span data-ttu-id="26f0b-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26f0b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f0b-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26f0b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f0b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f0b-144">CommonParameters</span></span>
<span data-ttu-id="26f0b-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="26f0b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f0b-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26f0b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f0b-147">輸入</span><span class="sxs-lookup"><span data-stu-id="26f0b-147">INPUTS</span></span>

## <span data-ttu-id="26f0b-148">輸出</span><span class="sxs-lookup"><span data-stu-id="26f0b-148">OUTPUTS</span></span>

### <span data-ttu-id="26f0b-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="26f0b-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="26f0b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="26f0b-150">NOTES</span></span>

<span data-ttu-id="26f0b-151">別名</span><span class="sxs-lookup"><span data-stu-id="26f0b-151">ALIASES</span></span>

## <span data-ttu-id="26f0b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="26f0b-152">RELATED LINKS</span></span>

