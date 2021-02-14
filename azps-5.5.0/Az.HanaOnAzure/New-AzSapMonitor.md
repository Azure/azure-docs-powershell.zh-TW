---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140834"
---
# <span data-ttu-id="79953-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="79953-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="79953-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79953-102">SYNOPSIS</span></span>
<span data-ttu-id="79953-103">針對指定的訂閱、資源群組和資源名稱建立 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="79953-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="79953-104">句法</span><span class="sxs-lookup"><span data-stu-id="79953-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79953-105">說明</span><span class="sxs-lookup"><span data-stu-id="79953-105">DESCRIPTION</span></span>
<span data-ttu-id="79953-106">針對指定的訂閱、資源群組和資源名稱建立 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="79953-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="79953-107">示例</span><span class="sxs-lookup"><span data-stu-id="79953-107">EXAMPLES</span></span>

### <span data-ttu-id="79953-108">範例1：新的 SAP 監視器</span><span class="sxs-lookup"><span data-stu-id="79953-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="79953-109">這個命令會建立 SAP 監視器。</span><span class="sxs-lookup"><span data-stu-id="79953-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="79953-110">參數</span><span class="sxs-lookup"><span data-stu-id="79953-110">PARAMETERS</span></span>

### <span data-ttu-id="79953-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79953-111">-AsJob</span></span>
<span data-ttu-id="79953-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="79953-112">Run the command as a job</span></span>

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

### <span data-ttu-id="79953-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79953-113">-DefaultProfile</span></span>
<span data-ttu-id="79953-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79953-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79953-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="79953-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="79953-116">指示是否要傳送分析至 Microsoft 的值</span><span class="sxs-lookup"><span data-stu-id="79953-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="79953-117">-位置</span><span class="sxs-lookup"><span data-stu-id="79953-117">-Location</span></span>
<span data-ttu-id="79953-118">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="79953-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="79953-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="79953-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="79953-120">要用來進行監視的 log analytics 工作區的工作區識別碼</span><span class="sxs-lookup"><span data-stu-id="79953-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="79953-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="79953-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="79953-122">用於監視的 Log Analytics 工作區的 ARM 識別碼</span><span class="sxs-lookup"><span data-stu-id="79953-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="79953-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="79953-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="79953-124">用來進行監控的 log analytics 工作區共用金鑰</span><span class="sxs-lookup"><span data-stu-id="79953-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="79953-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="79953-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="79953-126">要部署 SAP 監視器的子網。</span><span class="sxs-lookup"><span data-stu-id="79953-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="79953-127">它應該是 HANA 資料庫的同一個子網。</span><span class="sxs-lookup"><span data-stu-id="79953-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="79953-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="79953-128">-Name</span></span>
<span data-ttu-id="79953-129">SAP 監視資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="79953-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="79953-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="79953-130">-NoWait</span></span>
<span data-ttu-id="79953-131">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="79953-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="79953-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79953-132">-ResourceGroupName</span></span>
<span data-ttu-id="79953-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79953-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="79953-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79953-134">-SubscriptionId</span></span>
<span data-ttu-id="79953-135">訂閱識別碼，可唯一識別 Microsoft Azure 訂閱。</span><span class="sxs-lookup"><span data-stu-id="79953-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="79953-136">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="79953-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="79953-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="79953-137">-Tag</span></span>
<span data-ttu-id="79953-138">資源標記。</span><span class="sxs-lookup"><span data-stu-id="79953-138">Resource tags.</span></span>

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

### <span data-ttu-id="79953-139">-確認</span><span class="sxs-lookup"><span data-stu-id="79953-139">-Confirm</span></span>
<span data-ttu-id="79953-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="79953-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79953-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79953-141">-WhatIf</span></span>
<span data-ttu-id="79953-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="79953-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79953-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79953-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79953-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79953-144">CommonParameters</span></span>
<span data-ttu-id="79953-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79953-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79953-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="79953-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79953-147">輸入</span><span class="sxs-lookup"><span data-stu-id="79953-147">INPUTS</span></span>

## <span data-ttu-id="79953-148">輸出</span><span class="sxs-lookup"><span data-stu-id="79953-148">OUTPUTS</span></span>

### <span data-ttu-id="79953-149">ISapMonitor （HanaOnAzure）。 Api20200207Preview。</span><span class="sxs-lookup"><span data-stu-id="79953-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="79953-150">筆記</span><span class="sxs-lookup"><span data-stu-id="79953-150">NOTES</span></span>

<span data-ttu-id="79953-151">別名</span><span class="sxs-lookup"><span data-stu-id="79953-151">ALIASES</span></span>

## <span data-ttu-id="79953-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="79953-152">RELATED LINKS</span></span>

