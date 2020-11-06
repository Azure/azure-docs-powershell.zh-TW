---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 0e3e82f9dff96fed9e336f95aa44483e85f5ee44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447014"
---
# <span data-ttu-id="a39ac-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="a39ac-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="a39ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a39ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a39ac-103">在工作區中建立儲存洞察力。</span><span class="sxs-lookup"><span data-stu-id="a39ac-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a39ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="a39ac-104">SYNTAX</span></span>

### <span data-ttu-id="a39ac-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="a39ac-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a39ac-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a39ac-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a39ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="a39ac-107">DESCRIPTION</span></span>
<span data-ttu-id="a39ac-108">**新的-AzureRmOperationalInsightsStorageInsight** Cmdlet 會在現有的工作區中建立新的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="a39ac-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="a39ac-109">示例</span><span class="sxs-lookup"><span data-stu-id="a39ac-109">EXAMPLES</span></span>

### <span data-ttu-id="a39ac-110">範例1：依名稱建立儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="a39ac-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="a39ac-111">第一個命令使用 Get-AzureRmStorageAccount Cmdlet 來取得名為 ContosoStorage 的儲存空間帳戶，然後將它儲存在 $Storage 變數中。</span><span class="sxs-lookup"><span data-stu-id="a39ac-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>

<span data-ttu-id="a39ac-112">第二個命令會透過使用管線運算子來取得指定的儲存空間帳戶金鑰，然後將它儲存在 $StorageKey 變數中，將 $Storage 至 Get-AzureRmStorageAccountKey Cmdlet 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a39ac-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>

<span data-ttu-id="a39ac-113">最後一個命令會在名為 MyWorkspace 的工作區中，建立名為 MyStorageInsight 的儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="a39ac-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="a39ac-114">此儲存空間洞察力會在指定的儲存空間帳戶資源中使用 WADWindowsEventLogsTable 資料表中的資料。</span><span class="sxs-lookup"><span data-stu-id="a39ac-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="a39ac-115">範例2：使用工作區物件建立儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="a39ac-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="a39ac-116">第一個命令使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將它儲存在 $Workspace 變數中。</span><span class="sxs-lookup"><span data-stu-id="a39ac-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="a39ac-117">第二個命令使用 Get-AzureRmStorageAccount Cmdlet 來取得指定的儲存空間帳戶，然後將它儲存在 $Storage 變數中。</span><span class="sxs-lookup"><span data-stu-id="a39ac-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>

<span data-ttu-id="a39ac-118">第三個命令會透過使用管線運算子來取得指定的金鑰，然後將它儲存在 $StorageKey 變數中，將 $Storage 至 Get-AzureRmStorageAccountKey Cmdlet 的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="a39ac-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>

<span data-ttu-id="a39ac-119">最後一個命令會在 $Workspace 中定義的工作區中，建立名為 MyStorageInsight 的儲存空間見解。</span><span class="sxs-lookup"><span data-stu-id="a39ac-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="a39ac-120">儲存洞察力會在指定的儲存空間帳戶資源中使用 WADWindowsEventLogsTable 資料表中的資料。</span><span class="sxs-lookup"><span data-stu-id="a39ac-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="a39ac-121">參數</span><span class="sxs-lookup"><span data-stu-id="a39ac-121">PARAMETERS</span></span>

### <span data-ttu-id="a39ac-122">-容器</span><span class="sxs-lookup"><span data-stu-id="a39ac-122">-Containers</span></span>
<span data-ttu-id="a39ac-123">指定包含資料的容器清單。</span><span class="sxs-lookup"><span data-stu-id="a39ac-123">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39ac-124">-DefaultProfile</span></span>
<span data-ttu-id="a39ac-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a39ac-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a39ac-126">-Force</span></span>
<span data-ttu-id="a39ac-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a39ac-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a39ac-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a39ac-128">-Name</span></span>
<span data-ttu-id="a39ac-129">指定儲存空間洞察力的名稱。</span><span class="sxs-lookup"><span data-stu-id="a39ac-129">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39ac-130">-ResourceGroupName</span></span>
<span data-ttu-id="a39ac-131">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a39ac-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a39ac-132">-StorageAccountKey</span></span>
<span data-ttu-id="a39ac-133">指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="a39ac-133">Specifies the access key for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a39ac-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="a39ac-135">指定儲存空間帳戶的 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="a39ac-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="a39ac-136">您可以執行 Get-AzureRmStorageAccount Cmdlet 並存取結果的 *Id* 參數，以進行檢索。</span><span class="sxs-lookup"><span data-stu-id="a39ac-136">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-137">-資料表</span><span class="sxs-lookup"><span data-stu-id="a39ac-137">-Tables</span></span>
<span data-ttu-id="a39ac-138">指定提供資料的資料表清單。</span><span class="sxs-lookup"><span data-stu-id="a39ac-138">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-139">-工作區</span><span class="sxs-lookup"><span data-stu-id="a39ac-139">-Workspace</span></span>
<span data-ttu-id="a39ac-140">指定新的儲存空間洞察力的工作區。</span><span class="sxs-lookup"><span data-stu-id="a39ac-140">Specifies the workspace for the new Storage Insight.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a39ac-141">-WorkspaceName</span></span>
<span data-ttu-id="a39ac-142">指定現有工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="a39ac-142">Specifies the name of an existing workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-143">-確認</span><span class="sxs-lookup"><span data-stu-id="a39ac-143">-Confirm</span></span>
<span data-ttu-id="a39ac-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a39ac-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39ac-145">-WhatIf</span></span>
<span data-ttu-id="a39ac-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a39ac-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a39ac-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a39ac-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39ac-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39ac-148">CommonParameters</span></span>
<span data-ttu-id="a39ac-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a39ac-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39ac-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a39ac-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39ac-151">輸入</span><span class="sxs-lookup"><span data-stu-id="a39ac-151">INPUTS</span></span>

### <span data-ttu-id="a39ac-152">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a39ac-152">PSWorkspace</span></span>
<span data-ttu-id="a39ac-153">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="a39ac-153">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a39ac-154">輸出</span><span class="sxs-lookup"><span data-stu-id="a39ac-154">OUTPUTS</span></span>

### <span data-ttu-id="a39ac-155">PSStorageInsight 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="a39ac-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="a39ac-156">筆記</span><span class="sxs-lookup"><span data-stu-id="a39ac-156">NOTES</span></span>

## <span data-ttu-id="a39ac-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="a39ac-157">RELATED LINKS</span></span>

[<span data-ttu-id="a39ac-158">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a39ac-158">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="a39ac-159">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a39ac-159">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


