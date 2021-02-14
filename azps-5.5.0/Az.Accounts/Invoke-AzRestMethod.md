---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134243"
---
# <span data-ttu-id="56154-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="56154-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="56154-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56154-102">SYNOPSIS</span></span>
<span data-ttu-id="56154-103">僅針對 Azure 資源管理端點構造及執行 HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="56154-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="56154-104">句法</span><span class="sxs-lookup"><span data-stu-id="56154-104">SYNTAX</span></span>

### <span data-ttu-id="56154-105">ByPath (預設) </span><span class="sxs-lookup"><span data-stu-id="56154-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56154-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="56154-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56154-107">說明</span><span class="sxs-lookup"><span data-stu-id="56154-107">DESCRIPTION</span></span>
<span data-ttu-id="56154-108">僅針對 Azure 資源管理端點構造及執行 HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="56154-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="56154-109">示例</span><span class="sxs-lookup"><span data-stu-id="56154-109">EXAMPLES</span></span>

### <span data-ttu-id="56154-110">範例1</span><span class="sxs-lookup"><span data-stu-id="56154-110">Example 1</span></span>
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

<span data-ttu-id="56154-111">透過路徑取得 log analytics 工作區</span><span class="sxs-lookup"><span data-stu-id="56154-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="56154-112">參數</span><span class="sxs-lookup"><span data-stu-id="56154-112">PARAMETERS</span></span>

### <span data-ttu-id="56154-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="56154-113">-ApiVersion</span></span>
<span data-ttu-id="56154-114">Api 版本</span><span class="sxs-lookup"><span data-stu-id="56154-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56154-115">-AsJob</span></span>
<span data-ttu-id="56154-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="56154-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56154-117">-DefaultProfile</span></span>
<span data-ttu-id="56154-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56154-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-119">-方法</span><span class="sxs-lookup"><span data-stu-id="56154-119">-Method</span></span>
<span data-ttu-id="56154-120">Http 方法</span><span class="sxs-lookup"><span data-stu-id="56154-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="56154-121">-Name</span></span>
<span data-ttu-id="56154-122">目標資源名稱清單</span><span class="sxs-lookup"><span data-stu-id="56154-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-123">-Path</span><span class="sxs-lookup"><span data-stu-id="56154-123">-Path</span></span>
<span data-ttu-id="56154-124">目標路徑</span><span class="sxs-lookup"><span data-stu-id="56154-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-125">-負載</span><span class="sxs-lookup"><span data-stu-id="56154-125">-Payload</span></span>
<span data-ttu-id="56154-126">JSON 格式有效負載</span><span class="sxs-lookup"><span data-stu-id="56154-126">JSON format payload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56154-127">-ResourceGroupName</span></span>
<span data-ttu-id="56154-128">目標資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="56154-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="56154-129">-ResourceProviderName</span></span>
<span data-ttu-id="56154-130">目標資源提供者名稱</span><span class="sxs-lookup"><span data-stu-id="56154-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="56154-131">-ResourceType</span></span>
<span data-ttu-id="56154-132">目標資源類型的清單</span><span class="sxs-lookup"><span data-stu-id="56154-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56154-133">-SubscriptionId</span></span>
<span data-ttu-id="56154-134">目標訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="56154-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-135">-確認</span><span class="sxs-lookup"><span data-stu-id="56154-135">-Confirm</span></span>
<span data-ttu-id="56154-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="56154-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56154-137">-WhatIf</span></span>
<span data-ttu-id="56154-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56154-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56154-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56154-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56154-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56154-140">CommonParameters</span></span>
<span data-ttu-id="56154-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56154-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56154-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56154-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56154-143">輸入</span><span class="sxs-lookup"><span data-stu-id="56154-143">INPUTS</span></span>

### <span data-ttu-id="56154-144">System.object</span><span class="sxs-lookup"><span data-stu-id="56154-144">System.string</span></span>

## <span data-ttu-id="56154-145">輸出</span><span class="sxs-lookup"><span data-stu-id="56154-145">OUTPUTS</span></span>

### <span data-ttu-id="56154-146">PSHttpResponse 的設定檔。</span><span class="sxs-lookup"><span data-stu-id="56154-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="56154-147">筆記</span><span class="sxs-lookup"><span data-stu-id="56154-147">NOTES</span></span>

## <span data-ttu-id="56154-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="56154-148">RELATED LINKS</span></span>
