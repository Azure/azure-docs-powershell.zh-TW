---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: 4fb6a38ff9c79a16d150402d3a2e2be135e0c004
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970261"
---
# <span data-ttu-id="9a5da-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9a5da-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="9a5da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a5da-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5da-103">在 Azure Log Analytics 工作區中取得資料來源。</span><span class="sxs-lookup"><span data-stu-id="9a5da-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="9a5da-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a5da-104">SYNTAX</span></span>

### <span data-ttu-id="9a5da-105">ByWorkspaceNameByKind (預設) </span><span class="sxs-lookup"><span data-stu-id="9a5da-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a5da-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="9a5da-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a5da-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="9a5da-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a5da-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="9a5da-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a5da-109">說明</span><span class="sxs-lookup"><span data-stu-id="9a5da-109">DESCRIPTION</span></span>
<span data-ttu-id="9a5da-110">**AzOperationalInsightsDataSource** Cmdlet 會取得資料來源。</span><span class="sxs-lookup"><span data-stu-id="9a5da-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="9a5da-111">您可以指定要取得的資料來源。</span><span class="sxs-lookup"><span data-stu-id="9a5da-111">You can specify a data source to get.</span></span>
<span data-ttu-id="9a5da-112">您可以根據資料來源的類型來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="9a5da-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="9a5da-113">示例</span><span class="sxs-lookup"><span data-stu-id="9a5da-113">EXAMPLES</span></span>

## <span data-ttu-id="9a5da-114">參數</span><span class="sxs-lookup"><span data-stu-id="9a5da-114">PARAMETERS</span></span>

### <span data-ttu-id="9a5da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5da-115">-DefaultProfile</span></span>
<span data-ttu-id="9a5da-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9a5da-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a5da-117">類型</span><span class="sxs-lookup"><span data-stu-id="9a5da-117">-Kind</span></span>
<span data-ttu-id="9a5da-118">指定要取得的資料來源類型。</span><span class="sxs-lookup"><span data-stu-id="9a5da-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="9a5da-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9a5da-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a5da-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="9a5da-120">AzureActivityLog</span></span> 
- <span data-ttu-id="9a5da-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="9a5da-121">CustomLog</span></span> 
- <span data-ttu-id="9a5da-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="9a5da-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="9a5da-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="9a5da-123">LinuxSyslog</span></span> 
- <span data-ttu-id="9a5da-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="9a5da-124">WindowsEvent</span></span> 
- <span data-ttu-id="9a5da-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="9a5da-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5da-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a5da-126">-Name</span></span>
<span data-ttu-id="9a5da-127">指定要取得的資料來源名稱。</span><span class="sxs-lookup"><span data-stu-id="9a5da-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="9a5da-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a5da-128">-ResourceGroupName</span></span>
<span data-ttu-id="9a5da-129">指定包含要取得之資料來源的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a5da-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5da-130">-工作區</span><span class="sxs-lookup"><span data-stu-id="9a5da-130">-Workspace</span></span>
<span data-ttu-id="9a5da-131">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="9a5da-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9a5da-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a5da-132">-WorkspaceName</span></span>
<span data-ttu-id="9a5da-133">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="9a5da-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5da-134">CommonParameters</span></span>
<span data-ttu-id="9a5da-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a5da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5da-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a5da-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5da-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9a5da-137">INPUTS</span></span>

### <span data-ttu-id="9a5da-138">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="9a5da-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="9a5da-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9a5da-139">System.String</span></span>

## <span data-ttu-id="9a5da-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9a5da-140">OUTPUTS</span></span>

### <span data-ttu-id="9a5da-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="9a5da-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="9a5da-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9a5da-142">NOTES</span></span>
* <span data-ttu-id="9a5da-143">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="9a5da-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="9a5da-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a5da-144">RELATED LINKS</span></span>

[<span data-ttu-id="9a5da-145">移除-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9a5da-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="9a5da-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="9a5da-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


