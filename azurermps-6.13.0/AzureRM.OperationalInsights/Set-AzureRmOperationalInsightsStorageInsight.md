---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 460a1585c8c6c556f0044b9cd0673a3be750ffe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623908"
---
# <span data-ttu-id="6ff4e-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="6ff4e-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="6ff4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ff4e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff4e-103">更新儲存空間洞察力。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ff4e-104">SYNTAX</span></span>

### <span data-ttu-id="6ff4e-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="6ff4e-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ff4e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6ff4e-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff4e-107">說明</span><span class="sxs-lookup"><span data-stu-id="6ff4e-107">DESCRIPTION</span></span>
<span data-ttu-id="6ff4e-108">AzureRmOperationalInsightsStorageInsight Cmdlet 會變更儲存空間洞察力的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="6ff4e-109">示例</span><span class="sxs-lookup"><span data-stu-id="6ff4e-109">EXAMPLES</span></span>

### <span data-ttu-id="6ff4e-110">範例1：依名稱修改儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="6ff4e-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="6ff4e-111">這個命令會修改名為 [MyStorageInsight 讀取] 的儲存空間。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="6ff4e-112">範例2：使用工作區物件修改儲存空間洞察力</span><span class="sxs-lookup"><span data-stu-id="6ff4e-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="6ff4e-113">第一個命令使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將它儲存在 $Workspace 變數中。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="6ff4e-114">第二個命令會修改名為 MyStorageInsight 讀取之儲存空間洞察力的容器。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="6ff4e-115">參數</span><span class="sxs-lookup"><span data-stu-id="6ff4e-115">PARAMETERS</span></span>

### <span data-ttu-id="6ff4e-116">-容器</span><span class="sxs-lookup"><span data-stu-id="6ff4e-116">-Containers</span></span>
<span data-ttu-id="6ff4e-117">指定提供資料的容器清單。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="6ff4e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff4e-118">-DefaultProfile</span></span>
<span data-ttu-id="6ff4e-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6ff4e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff4e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ff4e-120">-Name</span></span>
<span data-ttu-id="6ff4e-121">指定儲存空間洞察力的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="6ff4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ff4e-123">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="6ff4e-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6ff4e-124">-StorageAccountKey</span></span>
<span data-ttu-id="6ff4e-125">指定儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff4e-126">-資料表</span><span class="sxs-lookup"><span data-stu-id="6ff4e-126">-Tables</span></span>
<span data-ttu-id="6ff4e-127">指定包含資料的資料表清單。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff4e-128">-工作區</span><span class="sxs-lookup"><span data-stu-id="6ff4e-128">-Workspace</span></span>
<span data-ttu-id="6ff4e-129">指定包含儲存空間洞察力的工作區。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="6ff4e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6ff4e-130">-WorkspaceName</span></span>
<span data-ttu-id="6ff4e-131">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="6ff4e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff4e-132">CommonParameters</span></span>
<span data-ttu-id="6ff4e-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff4e-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff4e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6ff4e-135">INPUTS</span></span>

### <span data-ttu-id="6ff4e-136">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="6ff4e-137">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="6ff4e-137">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="6ff4e-138">System.object</span><span class="sxs-lookup"><span data-stu-id="6ff4e-138">System.String</span></span>

### <span data-ttu-id="6ff4e-139">System.object []</span><span class="sxs-lookup"><span data-stu-id="6ff4e-139">System.String[]</span></span>

## <span data-ttu-id="6ff4e-140">輸出</span><span class="sxs-lookup"><span data-stu-id="6ff4e-140">OUTPUTS</span></span>

### <span data-ttu-id="6ff4e-141">PSStorageInsight 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="6ff4e-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="6ff4e-142">筆記</span><span class="sxs-lookup"><span data-stu-id="6ff4e-142">NOTES</span></span>

## <span data-ttu-id="6ff4e-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ff4e-143">RELATED LINKS</span></span>

[<span data-ttu-id="6ff4e-144">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ff4e-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="6ff4e-145">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="6ff4e-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


