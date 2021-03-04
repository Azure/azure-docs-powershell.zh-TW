---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: f3ab3c381e36c766e6d4bdb24476f6bd1cd69df3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911594"
---
# <span data-ttu-id="ddda9-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ddda9-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="ddda9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ddda9-102">SYNOPSIS</span></span>
<span data-ttu-id="ddda9-103">在工作區內建立儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="ddda9-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="ddda9-104">語法</span><span class="sxs-lookup"><span data-stu-id="ddda9-104">SYNTAX</span></span>

### <span data-ttu-id="ddda9-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="ddda9-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddda9-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ddda9-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddda9-107">描述</span><span class="sxs-lookup"><span data-stu-id="ddda9-107">DESCRIPTION</span></span>
<span data-ttu-id="ddda9-108">**New-AzOperationalInsightsStorageInsight** Cmdlet 會對現有工作區建立新的儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="ddda9-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="ddda9-109">例子</span><span class="sxs-lookup"><span data-stu-id="ddda9-109">EXAMPLES</span></span>

### <span data-ttu-id="ddda9-110">範例 1：根據名稱建立儲存深入資訊</span><span class="sxs-lookup"><span data-stu-id="ddda9-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="ddda9-111">第一個命令使用 Get-AzStorageAccount Cmdlet 取得名為 ContosoStorage 的儲存空間帳戶，然後將它儲存在 $Storage 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddda9-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="ddda9-112">第二個命令會使用管線運算子，將 $Storage 中的儲存空間帳戶傳遞至 Get-AzStorageAccountKey Cmdlet，以取得指定的儲存帳戶金鑰，然後將它儲存在 $StorageKey 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddda9-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="ddda9-113">此範例會取回第一個金鑰。</span><span class="sxs-lookup"><span data-stu-id="ddda9-113">This example retrieves the first key.</span></span> <span data-ttu-id="ddda9-114">若要取回另一個，請使用 Value[1] 而不是 Value[0]。</span><span class="sxs-lookup"><span data-stu-id="ddda9-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="ddda9-115">最後一個命令在名為 MyWorkspace 的工作區中，建立名為 MyStorageInsight 的儲存深入資訊。</span><span class="sxs-lookup"><span data-stu-id="ddda9-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="ddda9-116">此儲存深入資訊會耗用指定儲存帳戶資源中 WADWindowsEventLogsTable 資料表的資料。</span><span class="sxs-lookup"><span data-stu-id="ddda9-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="ddda9-117">範例 2：使用工作區物件建立儲存空間深入資訊</span><span class="sxs-lookup"><span data-stu-id="ddda9-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="ddda9-118">第一個命令使用 Get-AzOperationalInsightsWorkspace Cmdlet 取得名為 MyWorkspace 的工作區，然後將它儲存在 $Workspace 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddda9-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="ddda9-119">第二個命令使用 Get-AzStorageAccount Cmdlet 取得指定的儲存空間帳戶，然後將它儲存在 $Storage 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddda9-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="ddda9-120">第三個命令會使用管線運算子將 $Storage 中的儲存空間帳戶傳遞至 Get-AzStorageAccountKey Cmdlet，以取得指定的金鑰，然後將它儲存在 $StorageKey 變數中。</span><span class="sxs-lookup"><span data-stu-id="ddda9-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="ddda9-121">此範例會取回第一個金鑰。</span><span class="sxs-lookup"><span data-stu-id="ddda9-121">This example retrieves the first key.</span></span> <span data-ttu-id="ddda9-122">若要取回另一個，請使用 Value[1] 而不是 Value[0]。</span><span class="sxs-lookup"><span data-stu-id="ddda9-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="ddda9-123">最後一個命令在 $Workspace 中定義的工作區中，建立名為 MyStorageInsight 的儲存$Workspace。</span><span class="sxs-lookup"><span data-stu-id="ddda9-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="ddda9-124">儲存深入資訊會耗用指定儲存帳戶資源中 WADWindowsEventLogsTable 資料表的資料。</span><span class="sxs-lookup"><span data-stu-id="ddda9-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="ddda9-125">參數</span><span class="sxs-lookup"><span data-stu-id="ddda9-125">PARAMETERS</span></span>

### <span data-ttu-id="ddda9-126">-容器</span><span class="sxs-lookup"><span data-stu-id="ddda9-126">-Containers</span></span>
<span data-ttu-id="ddda9-127">指定包含資料的容器清單。</span><span class="sxs-lookup"><span data-stu-id="ddda9-127">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddda9-128">-DefaultProfile</span></span>
<span data-ttu-id="ddda9-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="ddda9-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddda9-130">-強制</span><span class="sxs-lookup"><span data-stu-id="ddda9-130">-Force</span></span>
<span data-ttu-id="ddda9-131">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ddda9-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ddda9-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddda9-132">-Name</span></span>
<span data-ttu-id="ddda9-133">指定儲存深入資訊的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddda9-133">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddda9-134">-ResourceGroupName</span></span>
<span data-ttu-id="ddda9-135">指定包含工作區的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="ddda9-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ddda9-136">-StorageAccountKey</span></span>
<span data-ttu-id="ddda9-137">指定儲存空間帳戶的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="ddda9-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ddda9-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="ddda9-139">指定儲存帳戶的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="ddda9-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="ddda9-140">您可以執行 Cmdlet Get-AzStorageAccount存取結果 *的 Id* 參數，以取得此結果。</span><span class="sxs-lookup"><span data-stu-id="ddda9-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-141">-表格</span><span class="sxs-lookup"><span data-stu-id="ddda9-141">-Tables</span></span>
<span data-ttu-id="ddda9-142">指定提供資料的表格清單。</span><span class="sxs-lookup"><span data-stu-id="ddda9-142">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-143">-工作區</span><span class="sxs-lookup"><span data-stu-id="ddda9-143">-Workspace</span></span>
<span data-ttu-id="ddda9-144">指定新儲存深入資訊工作區。</span><span class="sxs-lookup"><span data-stu-id="ddda9-144">Specifies the workspace for the new Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ddda9-145">-WorkspaceName</span></span>
<span data-ttu-id="ddda9-146">指定現有工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddda9-146">Specifies the name of an existing workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-147">-確認</span><span class="sxs-lookup"><span data-stu-id="ddda9-147">-Confirm</span></span>
<span data-ttu-id="ddda9-148">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ddda9-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddda9-149">-WhatIf</span></span>
<span data-ttu-id="ddda9-150">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddda9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddda9-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddda9-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddda9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddda9-152">CommonParameters</span></span>
<span data-ttu-id="ddda9-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ddda9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddda9-154">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ddda9-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddda9-155">輸入</span><span class="sxs-lookup"><span data-stu-id="ddda9-155">INPUTS</span></span>

### <span data-ttu-id="ddda9-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ddda9-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ddda9-157">System.String</span><span class="sxs-lookup"><span data-stu-id="ddda9-157">System.String</span></span>

### <span data-ttu-id="ddda9-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ddda9-158">System.String[]</span></span>

## <span data-ttu-id="ddda9-159">輸出</span><span class="sxs-lookup"><span data-stu-id="ddda9-159">OUTPUTS</span></span>

### <span data-ttu-id="ddda9-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ddda9-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="ddda9-161">筆記</span><span class="sxs-lookup"><span data-stu-id="ddda9-161">NOTES</span></span>

## <span data-ttu-id="ddda9-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddda9-162">RELATED LINKS</span></span>

[<span data-ttu-id="ddda9-163">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddda9-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="ddda9-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ddda9-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


