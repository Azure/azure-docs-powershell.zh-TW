---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: 355de1e4eb4518b8ec3d7291b20f76bda5fb1a89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902677"
---
# <span data-ttu-id="301c2-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="301c2-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="301c2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="301c2-102">SYNOPSIS</span></span>
<span data-ttu-id="301c2-103">僅建構和執行 Azure 資源管理端點的 HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="301c2-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="301c2-104">語法</span><span class="sxs-lookup"><span data-stu-id="301c2-104">SYNTAX</span></span>

### <span data-ttu-id="301c2-105">ByPath (預設) </span><span class="sxs-lookup"><span data-stu-id="301c2-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="301c2-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="301c2-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="301c2-107">描述</span><span class="sxs-lookup"><span data-stu-id="301c2-107">DESCRIPTION</span></span>
<span data-ttu-id="301c2-108">僅建構和執行 Azure 資源管理端點的 HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="301c2-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="301c2-109">例子</span><span class="sxs-lookup"><span data-stu-id="301c2-109">EXAMPLES</span></span>

### <span data-ttu-id="301c2-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="301c2-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="301c2-111">根據路徑取得記錄分析工作區</span><span class="sxs-lookup"><span data-stu-id="301c2-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="301c2-112">參數</span><span class="sxs-lookup"><span data-stu-id="301c2-112">PARAMETERS</span></span>

### <span data-ttu-id="301c2-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="301c2-113">-ApiVersion</span></span>
<span data-ttu-id="301c2-114">Api 版本</span><span class="sxs-lookup"><span data-stu-id="301c2-114">Api Version</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="301c2-115">-AsJob</span></span>
<span data-ttu-id="301c2-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="301c2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="301c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301c2-117">-DefaultProfile</span></span>
<span data-ttu-id="301c2-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="301c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-119">-方法</span><span class="sxs-lookup"><span data-stu-id="301c2-119">-Method</span></span>
<span data-ttu-id="301c2-120">Http 方法</span><span class="sxs-lookup"><span data-stu-id="301c2-120">Http Method</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="301c2-121">-Name</span></span>
<span data-ttu-id="301c2-122">目標資源名稱清單</span><span class="sxs-lookup"><span data-stu-id="301c2-122">list of Target Resource Name</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-123">-路徑</span><span class="sxs-lookup"><span data-stu-id="301c2-123">-Path</span></span>
<span data-ttu-id="301c2-124">目標路徑</span><span class="sxs-lookup"><span data-stu-id="301c2-124">Target Path</span></span>

```yaml
Type: System.String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-125">-有效負載</span><span class="sxs-lookup"><span data-stu-id="301c2-125">-Payload</span></span>
<span data-ttu-id="301c2-126">JSON 格式負載</span><span class="sxs-lookup"><span data-stu-id="301c2-126">JSON format payload</span></span>

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

### <span data-ttu-id="301c2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="301c2-127">-ResourceGroupName</span></span>
<span data-ttu-id="301c2-128">目標資源組名</span><span class="sxs-lookup"><span data-stu-id="301c2-128">Target Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="301c2-129">-ResourceProviderName</span></span>
<span data-ttu-id="301c2-130">目標資源提供者名稱</span><span class="sxs-lookup"><span data-stu-id="301c2-130">Target Resource Provider Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="301c2-131">-ResourceType</span></span>
<span data-ttu-id="301c2-132">目標資源類型清單</span><span class="sxs-lookup"><span data-stu-id="301c2-132">List of Target Resource Type</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="301c2-133">-SubscriptionId</span></span>
<span data-ttu-id="301c2-134">目標訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="301c2-134">Target Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301c2-135">-確認</span><span class="sxs-lookup"><span data-stu-id="301c2-135">-Confirm</span></span>
<span data-ttu-id="301c2-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="301c2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="301c2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="301c2-137">-WhatIf</span></span>
<span data-ttu-id="301c2-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="301c2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="301c2-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="301c2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="301c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301c2-140">CommonParameters</span></span>
<span data-ttu-id="301c2-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="301c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301c2-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="301c2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301c2-143">輸入</span><span class="sxs-lookup"><span data-stu-id="301c2-143">INPUTS</span></span>

### <span data-ttu-id="301c2-144">System.string</span><span class="sxs-lookup"><span data-stu-id="301c2-144">System.string</span></span>

## <span data-ttu-id="301c2-145">輸出</span><span class="sxs-lookup"><span data-stu-id="301c2-145">OUTPUTS</span></span>

### <span data-ttu-id="301c2-146">Microsoft.Azure.Commands.Profile.models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="301c2-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="301c2-147">筆記</span><span class="sxs-lookup"><span data-stu-id="301c2-147">NOTES</span></span>

## <span data-ttu-id="301c2-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="301c2-148">RELATED LINKS</span></span>
