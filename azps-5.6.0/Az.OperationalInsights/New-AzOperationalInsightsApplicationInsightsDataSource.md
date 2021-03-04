---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 21de9e423134c78302adf5c172dee0869b9501bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916901"
---
# <span data-ttu-id="420a4-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="420a4-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="420a4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="420a4-102">SYNOPSIS</span></span>
<span data-ttu-id="420a4-103">從給定應用程式收集Application-Insights記錄。</span><span class="sxs-lookup"><span data-stu-id="420a4-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="420a4-104">語法</span><span class="sxs-lookup"><span data-stu-id="420a4-104">SYNTAX</span></span>

### <span data-ttu-id="420a4-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="420a4-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="420a4-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="420a4-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="420a4-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="420a4-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="420a4-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="420a4-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="420a4-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="420a4-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="420a4-110">描述</span><span class="sxs-lookup"><span data-stu-id="420a4-110">DESCRIPTION</span></span>
<span data-ttu-id="420a4-111">**New-AzOperationalInsightsApplicationInsightsDataSource** Cmdlet 可啟用來自Application-Insights記錄的集合。</span><span class="sxs-lookup"><span data-stu-id="420a4-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="420a4-112">例子</span><span class="sxs-lookup"><span data-stu-id="420a4-112">EXAMPLES</span></span>

### <span data-ttu-id="420a4-113">範例 1：在工作區中建立應用程式深入資訊資料來源</span><span class="sxs-lookup"><span data-stu-id="420a4-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="420a4-114">此命令在給定記錄分析工作區中，為一個給定應用程式建立應用程式深入解析資料來源。</span><span class="sxs-lookup"><span data-stu-id="420a4-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="420a4-115">這可讓從給定應用程式到記錄分析工作區的記錄集合。</span><span class="sxs-lookup"><span data-stu-id="420a4-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="420a4-116">範例 2：取得工作區物件，然後根據應用程式資源識別碼建立應用程式深入資訊資料來源</span><span class="sxs-lookup"><span data-stu-id="420a4-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="420a4-117">此命令示範取得記錄分析工作區物件，然後傳遞輸出，以應用程式資源識別碼建立相關聯的應用程式深入解析資料來源。</span><span class="sxs-lookup"><span data-stu-id="420a4-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="420a4-118">參數</span><span class="sxs-lookup"><span data-stu-id="420a4-118">PARAMETERS</span></span>

### <span data-ttu-id="420a4-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="420a4-119">-ApplicationName</span></span>
<span data-ttu-id="420a4-120">連結應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="420a4-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420a4-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="420a4-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="420a4-122">連結應用程式的資源組名。</span><span class="sxs-lookup"><span data-stu-id="420a4-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420a4-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="420a4-123">-ApplicationResourceId</span></span>
<span data-ttu-id="420a4-124">連結的應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="420a4-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420a4-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="420a4-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="420a4-126">連結應用程式的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="420a4-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420a4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420a4-127">-DefaultProfile</span></span>
<span data-ttu-id="420a4-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="420a4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="420a4-129">-強制</span><span class="sxs-lookup"><span data-stu-id="420a4-129">-Force</span></span>
<span data-ttu-id="420a4-130">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="420a4-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="420a4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="420a4-131">-ResourceGroupName</span></span>
<span data-ttu-id="420a4-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="420a4-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420a4-133">-工作區</span><span class="sxs-lookup"><span data-stu-id="420a4-133">-Workspace</span></span>
<span data-ttu-id="420a4-134">包含資料來源的工作區。</span><span class="sxs-lookup"><span data-stu-id="420a4-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="420a4-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="420a4-135">-WorkspaceName</span></span>
<span data-ttu-id="420a4-136">包含資料來源的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="420a4-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420a4-137">-確認</span><span class="sxs-lookup"><span data-stu-id="420a4-137">-Confirm</span></span>
<span data-ttu-id="420a4-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="420a4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="420a4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="420a4-139">-WhatIf</span></span>
<span data-ttu-id="420a4-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="420a4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="420a4-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="420a4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="420a4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420a4-142">CommonParameters</span></span>
<span data-ttu-id="420a4-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="420a4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420a4-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="420a4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420a4-145">輸入</span><span class="sxs-lookup"><span data-stu-id="420a4-145">INPUTS</span></span>

### <span data-ttu-id="420a4-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="420a4-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="420a4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="420a4-147">System.String</span></span>

## <span data-ttu-id="420a4-148">輸出</span><span class="sxs-lookup"><span data-stu-id="420a4-148">OUTPUTS</span></span>

### <span data-ttu-id="420a4-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="420a4-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="420a4-150">筆記</span><span class="sxs-lookup"><span data-stu-id="420a4-150">NOTES</span></span>

## <span data-ttu-id="420a4-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="420a4-151">RELATED LINKS</span></span>
