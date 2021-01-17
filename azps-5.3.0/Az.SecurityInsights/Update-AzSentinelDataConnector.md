---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448499"
---
# <span data-ttu-id="454f8-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="454f8-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="454f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="454f8-102">SYNOPSIS</span></span>
<span data-ttu-id="454f8-103">更新資料連線器。</span><span class="sxs-lookup"><span data-stu-id="454f8-103">Update a Data Connector.</span></span>

## <span data-ttu-id="454f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="454f8-104">SYNTAX</span></span>

### <span data-ttu-id="454f8-105">DataConnectorId (預設) </span><span class="sxs-lookup"><span data-stu-id="454f8-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454f8-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="454f8-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454f8-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="454f8-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="454f8-108">說明</span><span class="sxs-lookup"><span data-stu-id="454f8-108">DESCRIPTION</span></span>
<span data-ttu-id="454f8-109">**更新-AzSentinelDataConnector** Cmdlet 會更新指定工作區中的資料連線器。</span><span class="sxs-lookup"><span data-stu-id="454f8-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="454f8-110">您可以將 **DataConnector** 物件傳遞為參數或使用管線運算子，或者也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="454f8-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="454f8-111">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="454f8-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="454f8-112">示例</span><span class="sxs-lookup"><span data-stu-id="454f8-112">EXAMPLES</span></span>

### <span data-ttu-id="454f8-113">範例1</span><span class="sxs-lookup"><span data-stu-id="454f8-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="454f8-114">命令會透過 *DataConnectorId* 取得資料連線器，並將 [ *警示* ] 狀態設為 [ *停用*]。</span><span class="sxs-lookup"><span data-stu-id="454f8-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="454f8-115">所有其他屬性都保持不變。</span><span class="sxs-lookup"><span data-stu-id="454f8-115">All other properties remain the same.</span></span>

## <span data-ttu-id="454f8-116">參數</span><span class="sxs-lookup"><span data-stu-id="454f8-116">PARAMETERS</span></span>

### <span data-ttu-id="454f8-117">-提醒</span><span class="sxs-lookup"><span data-stu-id="454f8-117">-Alerts</span></span>
<span data-ttu-id="454f8-118">資料連線器通知</span><span class="sxs-lookup"><span data-stu-id="454f8-118">Data Connector Alerts</span></span>

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

### <span data-ttu-id="454f8-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="454f8-119">-AwsRoleArn</span></span>
<span data-ttu-id="454f8-120">資料連線器 AWS 角色 Arn</span><span class="sxs-lookup"><span data-stu-id="454f8-120">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="454f8-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="454f8-121">-DataConnectorId</span></span>
<span data-ttu-id="454f8-122">資料連線器識別碼。</span><span class="sxs-lookup"><span data-stu-id="454f8-122">Data Connector Id.</span></span>

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

### <span data-ttu-id="454f8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="454f8-123">-DefaultProfile</span></span>
<span data-ttu-id="454f8-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="454f8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="454f8-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="454f8-125">-DiscoveryLogs</span></span>
<span data-ttu-id="454f8-126">資料連線器探索記錄</span><span class="sxs-lookup"><span data-stu-id="454f8-126">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="454f8-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="454f8-127">-Exchange</span></span>
<span data-ttu-id="454f8-128">資料連線器交換</span><span class="sxs-lookup"><span data-stu-id="454f8-128">Data Connector Exchange</span></span>

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

### <span data-ttu-id="454f8-129">-指標</span><span class="sxs-lookup"><span data-stu-id="454f8-129">-Indicators</span></span>
<span data-ttu-id="454f8-130">資料連線器標記</span><span class="sxs-lookup"><span data-stu-id="454f8-130">Data Connector Indicators</span></span>

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

### <span data-ttu-id="454f8-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="454f8-131">-InputObject</span></span>
<span data-ttu-id="454f8-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="454f8-132">InputObject.</span></span>

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

### <span data-ttu-id="454f8-133">-記錄</span><span class="sxs-lookup"><span data-stu-id="454f8-133">-Logs</span></span>
<span data-ttu-id="454f8-134">資料連線器記錄</span><span class="sxs-lookup"><span data-stu-id="454f8-134">Data Connector Logs</span></span>

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

### <span data-ttu-id="454f8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="454f8-135">-ResourceGroupName</span></span>
<span data-ttu-id="454f8-136">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="454f8-136">Resource group name.</span></span>

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

### <span data-ttu-id="454f8-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="454f8-137">-ResourceId</span></span>
<span data-ttu-id="454f8-138">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="454f8-138">Resource Id.</span></span>

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

### <span data-ttu-id="454f8-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="454f8-139">-SharePoint</span></span>
<span data-ttu-id="454f8-140">資料連線器 SharePoint</span><span class="sxs-lookup"><span data-stu-id="454f8-140">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="454f8-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="454f8-141">-SubscriptionId</span></span>
<span data-ttu-id="454f8-142">資料連線器訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="454f8-142">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="454f8-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="454f8-143">-WorkspaceName</span></span>
<span data-ttu-id="454f8-144">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="454f8-144">Workspace Name.</span></span>

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

### <span data-ttu-id="454f8-145">-確認</span><span class="sxs-lookup"><span data-stu-id="454f8-145">-Confirm</span></span>
<span data-ttu-id="454f8-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="454f8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="454f8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="454f8-147">-WhatIf</span></span>
<span data-ttu-id="454f8-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="454f8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="454f8-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="454f8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="454f8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="454f8-150">CommonParameters</span></span>
<span data-ttu-id="454f8-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="454f8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="454f8-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="454f8-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="454f8-153">輸入</span><span class="sxs-lookup"><span data-stu-id="454f8-153">INPUTS</span></span>

### <span data-ttu-id="454f8-154">SecurityInsights DataConnectors. PSSentinelDataConnector （）</span><span class="sxs-lookup"><span data-stu-id="454f8-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="454f8-155">System.object</span><span class="sxs-lookup"><span data-stu-id="454f8-155">System.String</span></span>

## <span data-ttu-id="454f8-156">輸出</span><span class="sxs-lookup"><span data-stu-id="454f8-156">OUTPUTS</span></span>

### <span data-ttu-id="454f8-157">SecurityInsights DataConnectors. PSSentinelDataConnector （）</span><span class="sxs-lookup"><span data-stu-id="454f8-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="454f8-158">筆記</span><span class="sxs-lookup"><span data-stu-id="454f8-158">NOTES</span></span>

## <span data-ttu-id="454f8-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="454f8-159">RELATED LINKS</span></span>
