---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281292"
---
# <span data-ttu-id="69573-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="69573-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="69573-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69573-102">SYNOPSIS</span></span>
<span data-ttu-id="69573-103">從指定的 Application-Insights 應用程式收集記錄。</span><span class="sxs-lookup"><span data-stu-id="69573-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="69573-104">句法</span><span class="sxs-lookup"><span data-stu-id="69573-104">SYNTAX</span></span>

### <span data-ttu-id="69573-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="69573-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69573-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="69573-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69573-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="69573-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69573-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="69573-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69573-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="69573-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69573-110">說明</span><span class="sxs-lookup"><span data-stu-id="69573-110">DESCRIPTION</span></span>
<span data-ttu-id="69573-111">**新的-AzOperationalInsightsApplicationInsightsDataSource** Cmdlet 可從特定的 Application-Insights 應用程式中收集記錄。</span><span class="sxs-lookup"><span data-stu-id="69573-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="69573-112">示例</span><span class="sxs-lookup"><span data-stu-id="69573-112">EXAMPLES</span></span>

### <span data-ttu-id="69573-113">範例1：在工作區中建立 application insights 資料來源</span><span class="sxs-lookup"><span data-stu-id="69573-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="69573-114">這個命令會在指定的 log analytics 工作區中建立特定應用程式的 application insights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="69573-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="69573-115">這可讓特定應用程式的記錄集合成為 log analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="69573-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="69573-116">範例2：取得工作區物件並依應用程式資源識別碼建立 application insights 資料來源</span><span class="sxs-lookup"><span data-stu-id="69573-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="69573-117">這個命令示範如何取得 log analytics 工作區物件，然後透過應用程式資源識別碼，傳送輸出來建立關聯的 application insights 資料來源。</span><span class="sxs-lookup"><span data-stu-id="69573-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="69573-118">參數</span><span class="sxs-lookup"><span data-stu-id="69573-118">PARAMETERS</span></span>

### <span data-ttu-id="69573-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="69573-119">-ApplicationName</span></span>
<span data-ttu-id="69573-120">連結應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="69573-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="69573-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69573-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="69573-122">連結之應用程式的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="69573-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="69573-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="69573-123">-ApplicationResourceId</span></span>
<span data-ttu-id="69573-124">連結的應用程式資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="69573-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="69573-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69573-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="69573-126">連結應用程式的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="69573-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="69573-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69573-127">-DefaultProfile</span></span>
<span data-ttu-id="69573-128">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69573-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69573-129">-Force</span><span class="sxs-lookup"><span data-stu-id="69573-129">-Force</span></span>
<span data-ttu-id="69573-130">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="69573-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="69573-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69573-131">-ResourceGroupName</span></span>
<span data-ttu-id="69573-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69573-132">The resource group name.</span></span>

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

### <span data-ttu-id="69573-133">-工作區</span><span class="sxs-lookup"><span data-stu-id="69573-133">-Workspace</span></span>
<span data-ttu-id="69573-134">將包含資料來源的工作區。</span><span class="sxs-lookup"><span data-stu-id="69573-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="69573-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="69573-135">-WorkspaceName</span></span>
<span data-ttu-id="69573-136">將包含資料來源的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="69573-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="69573-137">-確認</span><span class="sxs-lookup"><span data-stu-id="69573-137">-Confirm</span></span>
<span data-ttu-id="69573-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="69573-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69573-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69573-139">-WhatIf</span></span>
<span data-ttu-id="69573-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="69573-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69573-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69573-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69573-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69573-142">CommonParameters</span></span>
<span data-ttu-id="69573-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69573-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69573-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69573-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69573-145">輸入</span><span class="sxs-lookup"><span data-stu-id="69573-145">INPUTS</span></span>

### <span data-ttu-id="69573-146">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="69573-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="69573-147">System.object</span><span class="sxs-lookup"><span data-stu-id="69573-147">System.String</span></span>

## <span data-ttu-id="69573-148">輸出</span><span class="sxs-lookup"><span data-stu-id="69573-148">OUTPUTS</span></span>

### <span data-ttu-id="69573-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="69573-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="69573-150">筆記</span><span class="sxs-lookup"><span data-stu-id="69573-150">NOTES</span></span>

## <span data-ttu-id="69573-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="69573-151">RELATED LINKS</span></span>
