---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: 6ccb7b5a38a85d114e3bb93b594d838c61dcff4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907505"
---
# <span data-ttu-id="d8329-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="d8329-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="d8329-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d8329-102">SYNOPSIS</span></span>
<span data-ttu-id="d8329-103">更新資料連線器。</span><span class="sxs-lookup"><span data-stu-id="d8329-103">Update a Data Connector.</span></span>

## <span data-ttu-id="d8329-104">語法</span><span class="sxs-lookup"><span data-stu-id="d8329-104">SYNTAX</span></span>

### <span data-ttu-id="d8329-105">DataConnectorId (預設) </span><span class="sxs-lookup"><span data-stu-id="d8329-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8329-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d8329-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8329-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8329-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8329-108">描述</span><span class="sxs-lookup"><span data-stu-id="d8329-108">DESCRIPTION</span></span>
<span data-ttu-id="d8329-109">**Update-AzSentinelDataConnector** Cmdlet 會更新指定工作區中的資料連線器。</span><span class="sxs-lookup"><span data-stu-id="d8329-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="d8329-110">您可以將 **DataConnector 物件** 傳遞為參數，或是使用管線運算子，或者您也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="d8329-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="d8329-111">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d8329-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d8329-112">例子</span><span class="sxs-lookup"><span data-stu-id="d8329-112">EXAMPLES</span></span>

### <span data-ttu-id="d8329-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="d8329-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="d8329-114">該命令會按 *DataConnectorId* 獲得資料連線器，並且將 *通知狀態設定* 為 *已停用*。</span><span class="sxs-lookup"><span data-stu-id="d8329-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="d8329-115">所有其他屬性會保持相同。</span><span class="sxs-lookup"><span data-stu-id="d8329-115">All other properties remain the same.</span></span>

## <span data-ttu-id="d8329-116">參數</span><span class="sxs-lookup"><span data-stu-id="d8329-116">PARAMETERS</span></span>

### <span data-ttu-id="d8329-117">-通知</span><span class="sxs-lookup"><span data-stu-id="d8329-117">-Alerts</span></span>
<span data-ttu-id="d8329-118">資料連線器通知</span><span class="sxs-lookup"><span data-stu-id="d8329-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="d8329-119">-AwsRoleArn</span></span>
<span data-ttu-id="d8329-120">Data Connector AWS 角色 Arn</span><span class="sxs-lookup"><span data-stu-id="d8329-120">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="d8329-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="d8329-121">-DataConnectorId</span></span>
<span data-ttu-id="d8329-122">資料連線器識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8329-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8329-123">-DefaultProfile</span></span>
<span data-ttu-id="d8329-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8329-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8329-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="d8329-125">-DiscoveryLogs</span></span>
<span data-ttu-id="d8329-126">資料連線器探索記錄</span><span class="sxs-lookup"><span data-stu-id="d8329-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="d8329-127">-Exchange</span></span>
<span data-ttu-id="d8329-128">資料連線器 Exchange</span><span class="sxs-lookup"><span data-stu-id="d8329-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-129">-標記</span><span class="sxs-lookup"><span data-stu-id="d8329-129">-Indicators</span></span>
<span data-ttu-id="d8329-130">資料連線器指示器</span><span class="sxs-lookup"><span data-stu-id="d8329-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8329-131">-InputObject</span></span>
<span data-ttu-id="d8329-132">InputObject。</span><span class="sxs-lookup"><span data-stu-id="d8329-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-133">-記錄</span><span class="sxs-lookup"><span data-stu-id="d8329-133">-Logs</span></span>
<span data-ttu-id="d8329-134">資料連線器記錄</span><span class="sxs-lookup"><span data-stu-id="d8329-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8329-135">-ResourceGroupName</span></span>
<span data-ttu-id="d8329-136">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d8329-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8329-137">-ResourceId</span></span>
<span data-ttu-id="d8329-138">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8329-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="d8329-139">-SharePoint</span></span>
<span data-ttu-id="d8329-140">資料連線器 SharePoint</span><span class="sxs-lookup"><span data-stu-id="d8329-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8329-141">-SubscriptionId</span></span>
<span data-ttu-id="d8329-142">資料連線器訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="d8329-142">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="d8329-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8329-143">-WorkspaceName</span></span>
<span data-ttu-id="d8329-144">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d8329-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8329-145">-確認</span><span class="sxs-lookup"><span data-stu-id="d8329-145">-Confirm</span></span>
<span data-ttu-id="d8329-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d8329-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8329-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8329-147">-WhatIf</span></span>
<span data-ttu-id="d8329-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8329-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8329-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8329-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8329-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8329-150">CommonParameters</span></span>
<span data-ttu-id="d8329-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d8329-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8329-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8329-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8329-153">輸入</span><span class="sxs-lookup"><span data-stu-id="d8329-153">INPUTS</span></span>

### <span data-ttu-id="d8329-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="d8329-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="d8329-155">System.String</span><span class="sxs-lookup"><span data-stu-id="d8329-155">System.String</span></span>

## <span data-ttu-id="d8329-156">輸出</span><span class="sxs-lookup"><span data-stu-id="d8329-156">OUTPUTS</span></span>

### <span data-ttu-id="d8329-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="d8329-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="d8329-158">筆記</span><span class="sxs-lookup"><span data-stu-id="d8329-158">NOTES</span></span>

## <span data-ttu-id="d8329-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8329-159">RELATED LINKS</span></span>
