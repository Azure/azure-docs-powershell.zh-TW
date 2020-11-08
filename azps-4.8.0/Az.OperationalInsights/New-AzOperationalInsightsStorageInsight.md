---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970861"
---
# <span data-ttu-id="91f14-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="91f14-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="91f14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91f14-102">SYNOPSIS</span></span>
<span data-ttu-id="91f14-103">在工作區中建立儲存洞察力。</span><span class="sxs-lookup"><span data-stu-id="91f14-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="91f14-104">句法</span><span class="sxs-lookup"><span data-stu-id="91f14-104">SYNTAX</span></span>

### <span data-ttu-id="91f14-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="91f14-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91f14-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="91f14-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91f14-107">說明</span><span class="sxs-lookup"><span data-stu-id="91f14-107">DESCRIPTION</span></span>
<span data-ttu-id="91f14-108">**新的-AzOperationalInsightsStorageInsight** Cmdlet 會在現有的工作區中建立新的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="91f14-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="91f14-109">示例</span><span class="sxs-lookup"><span data-stu-id="91f14-109">EXAMPLES</span></span>

### <span data-ttu-id="91f14-110">範例1：依名稱建立儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="91f14-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="91f14-111">第一個命令使用 Get-AzStorageAccount Cmdlet 來取得名為 ContosoStorage 的儲存空間帳戶，然後將它儲存在 $Storage 變數中。</span><span class="sxs-lookup"><span data-stu-id="91f14-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="91f14-112">第二個命令會透過使用管線運算子來取得指定的儲存空間帳戶金鑰，然後將它儲存在 $StorageKey 變數中，將 $Storage 至 Get-AzStorageAccountKey Cmdlet 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="91f14-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="91f14-113">這個範例會檢索第一個索引鍵。</span><span class="sxs-lookup"><span data-stu-id="91f14-113">This example retrieves the first key.</span></span> <span data-ttu-id="91f14-114">若要檢索另一個值，請使用值 [1]，而不是值 [0]。</span><span class="sxs-lookup"><span data-stu-id="91f14-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="91f14-115">最後一個命令會在名為 MyWorkspace 的工作區中，建立名為 MyStorageInsight 的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="91f14-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="91f14-116">此儲存空間洞察力會在指定的儲存空間帳戶資源中使用 WADWindowsEventLogsTable 資料表中的資料。</span><span class="sxs-lookup"><span data-stu-id="91f14-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="91f14-117">範例2：使用工作區物件建立儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="91f14-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="91f14-118">第一個命令使用 Get-AzOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將它儲存在 $Workspace 變數中。</span><span class="sxs-lookup"><span data-stu-id="91f14-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="91f14-119">第二個命令使用 Get-AzStorageAccount Cmdlet 來取得指定的儲存空間帳戶，然後將它儲存在 $Storage 變數中。</span><span class="sxs-lookup"><span data-stu-id="91f14-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="91f14-120">第三個命令會透過使用管線運算子來取得指定的金鑰，然後將它儲存在 $StorageKey 變數中，將 $Storage 至 Get-AzStorageAccountKey Cmdlet 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="91f14-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="91f14-121">這個範例會檢索第一個索引鍵。</span><span class="sxs-lookup"><span data-stu-id="91f14-121">This example retrieves the first key.</span></span> <span data-ttu-id="91f14-122">若要檢索另一個值，請使用值 [1]，而不是值 [0]。</span><span class="sxs-lookup"><span data-stu-id="91f14-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="91f14-123">最後一個命令會在 $Workspace 中定義的工作區中，建立名為 MyStorageInsight 的儲存空間見解。</span><span class="sxs-lookup"><span data-stu-id="91f14-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="91f14-124">儲存洞察力會在指定的儲存空間帳戶資源中使用 WADWindowsEventLogsTable 資料表中的資料。</span><span class="sxs-lookup"><span data-stu-id="91f14-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="91f14-125">參數</span><span class="sxs-lookup"><span data-stu-id="91f14-125">PARAMETERS</span></span>

### <span data-ttu-id="91f14-126">-容器</span><span class="sxs-lookup"><span data-stu-id="91f14-126">-Containers</span></span>
<span data-ttu-id="91f14-127">指定包含資料的容器清單。</span><span class="sxs-lookup"><span data-stu-id="91f14-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="91f14-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f14-128">-DefaultProfile</span></span>
<span data-ttu-id="91f14-129">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="91f14-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91f14-130">-Force</span><span class="sxs-lookup"><span data-stu-id="91f14-130">-Force</span></span>
<span data-ttu-id="91f14-131">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="91f14-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91f14-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="91f14-132">-Name</span></span>
<span data-ttu-id="91f14-133">指定儲存空間洞察力的名稱。</span><span class="sxs-lookup"><span data-stu-id="91f14-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="91f14-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f14-134">-ResourceGroupName</span></span>
<span data-ttu-id="91f14-135">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91f14-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="91f14-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="91f14-136">-StorageAccountKey</span></span>
<span data-ttu-id="91f14-137">指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="91f14-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="91f14-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="91f14-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="91f14-139">指定儲存空間帳戶的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="91f14-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="91f14-140">您可以執行 Get-AzStorageAccount Cmdlet 並存取結果的 *Id* 參數，以進行檢索。</span><span class="sxs-lookup"><span data-stu-id="91f14-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="91f14-141">-資料表</span><span class="sxs-lookup"><span data-stu-id="91f14-141">-Tables</span></span>
<span data-ttu-id="91f14-142">指定提供資料的資料表清單。</span><span class="sxs-lookup"><span data-stu-id="91f14-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="91f14-143">-工作區</span><span class="sxs-lookup"><span data-stu-id="91f14-143">-Workspace</span></span>
<span data-ttu-id="91f14-144">指定新的儲存空間洞察力的工作區。</span><span class="sxs-lookup"><span data-stu-id="91f14-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="91f14-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="91f14-145">-WorkspaceName</span></span>
<span data-ttu-id="91f14-146">指定現有工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="91f14-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="91f14-147">-確認</span><span class="sxs-lookup"><span data-stu-id="91f14-147">-Confirm</span></span>
<span data-ttu-id="91f14-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91f14-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f14-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f14-149">-WhatIf</span></span>
<span data-ttu-id="91f14-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91f14-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91f14-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91f14-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f14-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f14-152">CommonParameters</span></span>
<span data-ttu-id="91f14-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91f14-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f14-154">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91f14-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f14-155">輸入</span><span class="sxs-lookup"><span data-stu-id="91f14-155">INPUTS</span></span>

### <span data-ttu-id="91f14-156">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="91f14-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="91f14-157">System.object</span><span class="sxs-lookup"><span data-stu-id="91f14-157">System.String</span></span>

### <span data-ttu-id="91f14-158">System.object []</span><span class="sxs-lookup"><span data-stu-id="91f14-158">System.String[]</span></span>

## <span data-ttu-id="91f14-159">輸出</span><span class="sxs-lookup"><span data-stu-id="91f14-159">OUTPUTS</span></span>

### <span data-ttu-id="91f14-160">PSStorageInsight 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="91f14-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="91f14-161">筆記</span><span class="sxs-lookup"><span data-stu-id="91f14-161">NOTES</span></span>

## <span data-ttu-id="91f14-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="91f14-162">RELATED LINKS</span></span>

[<span data-ttu-id="91f14-163">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="91f14-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="91f14-164">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="91f14-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)

