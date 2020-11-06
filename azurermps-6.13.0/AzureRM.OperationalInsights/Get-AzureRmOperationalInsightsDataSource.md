---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 5d13fb4c432a0b40fdfd90a5eea55ea44a8b6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447318"
---
# <span data-ttu-id="ce3aa-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ce3aa-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="ce3aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3aa-103">在 Azure Log Analytics 工作區中取得資料來源。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce3aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce3aa-104">SYNTAX</span></span>

### <span data-ttu-id="ce3aa-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="ce3aa-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce3aa-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="ce3aa-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce3aa-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="ce3aa-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce3aa-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="ce3aa-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce3aa-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="ce3aa-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce3aa-110">說明</span><span class="sxs-lookup"><span data-stu-id="ce3aa-110">DESCRIPTION</span></span>
<span data-ttu-id="ce3aa-111">**AzureRmOperationalInsightsDataSource** Cmdlet 會取得資料來源。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="ce3aa-112">您可以指定要取得的資料來源。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-112">You can specify a data source to get.</span></span>
<span data-ttu-id="ce3aa-113">您可以根據資料來源的類型來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="ce3aa-114">示例</span><span class="sxs-lookup"><span data-stu-id="ce3aa-114">EXAMPLES</span></span>

## <span data-ttu-id="ce3aa-115">參數</span><span class="sxs-lookup"><span data-stu-id="ce3aa-115">PARAMETERS</span></span>

### <span data-ttu-id="ce3aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3aa-116">-DefaultProfile</span></span>
<span data-ttu-id="ce3aa-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ce3aa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce3aa-118">類型</span><span class="sxs-lookup"><span data-stu-id="ce3aa-118">-Kind</span></span>
<span data-ttu-id="ce3aa-119">指定要取得的資料來源類型。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="ce3aa-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ce3aa-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce3aa-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="ce3aa-121">AzureActivityLog</span></span> 
- <span data-ttu-id="ce3aa-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="ce3aa-122">CustomLog</span></span> 
- <span data-ttu-id="ce3aa-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="ce3aa-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="ce3aa-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="ce3aa-124">LinuxSyslog</span></span> 
- <span data-ttu-id="ce3aa-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="ce3aa-125">WindowsEvent</span></span> 
- <span data-ttu-id="ce3aa-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="ce3aa-126">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3aa-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce3aa-127">-Name</span></span>
<span data-ttu-id="ce3aa-128">指定要取得的資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-128">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce3aa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce3aa-129">-ResourceGroupName</span></span>
<span data-ttu-id="ce3aa-130">指定包含要取得之資料來源的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3aa-131">-工作區</span><span class="sxs-lookup"><span data-stu-id="ce3aa-131">-Workspace</span></span>
<span data-ttu-id="ce3aa-132">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-132">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3aa-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce3aa-133">-WorkspaceName</span></span>
<span data-ttu-id="ce3aa-134">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce3aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3aa-135">CommonParameters</span></span>
<span data-ttu-id="ce3aa-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3aa-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3aa-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ce3aa-138">INPUTS</span></span>

### <span data-ttu-id="ce3aa-139">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="ce3aa-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="ce3aa-140">參數：工作區 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ce3aa-140">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="ce3aa-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ce3aa-141">System.String</span></span>

## <span data-ttu-id="ce3aa-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ce3aa-142">OUTPUTS</span></span>

### <span data-ttu-id="ce3aa-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ce3aa-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ce3aa-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ce3aa-144">NOTES</span></span>
* <span data-ttu-id="ce3aa-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="ce3aa-145">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="ce3aa-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce3aa-146">RELATED LINKS</span></span>

[<span data-ttu-id="ce3aa-147">移除-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ce3aa-147">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="ce3aa-148">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ce3aa-148">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


