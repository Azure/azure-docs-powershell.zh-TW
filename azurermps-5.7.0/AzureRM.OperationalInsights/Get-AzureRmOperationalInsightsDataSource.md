---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 057437e55fd7877154343bdbfc5f25d216412b8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449252"
---
# <span data-ttu-id="fd2e2-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="fd2e2-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="fd2e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd2e2-103">在 Azure Log Analytics 工作區中取得資料來源。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd2e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd2e2-104">SYNTAX</span></span>

### <span data-ttu-id="fd2e2-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="fd2e2-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd2e2-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="fd2e2-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd2e2-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="fd2e2-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd2e2-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="fd2e2-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd2e2-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="fd2e2-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd2e2-110">說明</span><span class="sxs-lookup"><span data-stu-id="fd2e2-110">DESCRIPTION</span></span>
<span data-ttu-id="fd2e2-111">**AzureRmOperationalInsightsDataSource** Cmdlet 會取得資料來源。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="fd2e2-112">您可以指定要取得的資料來源。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-112">You can specify a data source to get.</span></span>
<span data-ttu-id="fd2e2-113">您可以根據資料來源的類型來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="fd2e2-114">示例</span><span class="sxs-lookup"><span data-stu-id="fd2e2-114">EXAMPLES</span></span>

## <span data-ttu-id="fd2e2-115">參數</span><span class="sxs-lookup"><span data-stu-id="fd2e2-115">PARAMETERS</span></span>

### <span data-ttu-id="fd2e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd2e2-116">-DefaultProfile</span></span>
<span data-ttu-id="fd2e2-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fd2e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd2e2-118">類型</span><span class="sxs-lookup"><span data-stu-id="fd2e2-118">-Kind</span></span>
<span data-ttu-id="fd2e2-119">指定要取得的資料來源類型。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="fd2e2-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="fd2e2-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fd2e2-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="fd2e2-121">AzureActivityLog</span></span> 
- <span data-ttu-id="fd2e2-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="fd2e2-122">CustomLog</span></span> 
- <span data-ttu-id="fd2e2-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="fd2e2-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="fd2e2-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="fd2e2-124">LinuxSyslog</span></span> 
- <span data-ttu-id="fd2e2-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="fd2e2-125">WindowsEvent</span></span> 
- <span data-ttu-id="fd2e2-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="fd2e2-126">WindowsPerformanceCounter</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2e2-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd2e2-127">-Name</span></span>
<span data-ttu-id="fd2e2-128">指定要取得的資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-128">Specifies the name of a data source to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd2e2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd2e2-129">-ResourceGroupName</span></span>
<span data-ttu-id="fd2e2-130">指定包含要取得之資料來源的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2e2-131">-工作區</span><span class="sxs-lookup"><span data-stu-id="fd2e2-131">-Workspace</span></span>
<span data-ttu-id="fd2e2-132">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-132">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2e2-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fd2e2-133">-WorkspaceName</span></span>
<span data-ttu-id="fd2e2-134">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd2e2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd2e2-135">CommonParameters</span></span>
<span data-ttu-id="fd2e2-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd2e2-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fd2e2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd2e2-138">輸入</span><span class="sxs-lookup"><span data-stu-id="fd2e2-138">INPUTS</span></span>

### <span data-ttu-id="fd2e2-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd2e2-139">PSWorkspace</span></span>
<span data-ttu-id="fd2e2-140">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="fd2e2-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="fd2e2-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd2e2-141">PSWorkspace</span></span>
<span data-ttu-id="fd2e2-142">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="fd2e2-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="fd2e2-143">輸出</span><span class="sxs-lookup"><span data-stu-id="fd2e2-143">OUTPUTS</span></span>

### <span data-ttu-id="fd2e2-144">[System.object]。清單 ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="fd2e2-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="fd2e2-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="fd2e2-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fd2e2-146">筆記</span><span class="sxs-lookup"><span data-stu-id="fd2e2-146">NOTES</span></span>
* <span data-ttu-id="fd2e2-147">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="fd2e2-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="fd2e2-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd2e2-148">RELATED LINKS</span></span>

[<span data-ttu-id="fd2e2-149">移除-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="fd2e2-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="fd2e2-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="fd2e2-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


