---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: b827c9d133ff6fc0bb9df0e1e3e25c3eea23916f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447016"
---
# <span data-ttu-id="f5802-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="f5802-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="f5802-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5802-102">SYNOPSIS</span></span>
<span data-ttu-id="f5802-103">新增執行 Windows 作業系統之已連接的電腦的 Windows 效能計數器資料來源。</span><span class="sxs-lookup"><span data-stu-id="f5802-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5802-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5802-104">SYNTAX</span></span>

### <span data-ttu-id="f5802-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="f5802-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5802-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f5802-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5802-107">說明</span><span class="sxs-lookup"><span data-stu-id="f5802-107">DESCRIPTION</span></span>
<span data-ttu-id="f5802-108">**新的-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** Cmdlet 會針對執行 windows 作業系統的已連接電腦新增 Windows 效能計數器資料來源。</span><span class="sxs-lookup"><span data-stu-id="f5802-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="f5802-109">示例</span><span class="sxs-lookup"><span data-stu-id="f5802-109">EXAMPLES</span></span>

## <span data-ttu-id="f5802-110">參數</span><span class="sxs-lookup"><span data-stu-id="f5802-110">PARAMETERS</span></span>

### <span data-ttu-id="f5802-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="f5802-111">-CounterName</span></span>
<span data-ttu-id="f5802-112">指定計數器的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5802-112">Specifies the name of a counter.</span></span>

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

### <span data-ttu-id="f5802-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5802-113">-DefaultProfile</span></span>
<span data-ttu-id="f5802-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f5802-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5802-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f5802-115">-Force</span></span>
<span data-ttu-id="f5802-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f5802-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5802-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f5802-117">-InstanceName</span></span>
<span data-ttu-id="f5802-118">指定實例名稱。</span><span class="sxs-lookup"><span data-stu-id="f5802-118">Specifies an instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5802-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f5802-119">-IntervalSeconds</span></span>
<span data-ttu-id="f5802-120">指定集合的間隔。</span><span class="sxs-lookup"><span data-stu-id="f5802-120">Specifies the interval of collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5802-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5802-121">-Name</span></span>
<span data-ttu-id="f5802-122">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5802-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="f5802-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="f5802-123">-ObjectName</span></span>
<span data-ttu-id="f5802-124">指定物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5802-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="f5802-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5802-125">-ResourceGroupName</span></span>
<span data-ttu-id="f5802-126">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5802-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="f5802-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="f5802-127">-UseLegacyCollector</span></span>
<span data-ttu-id="f5802-128">使用舊版收集器或預設收集器。</span><span class="sxs-lookup"><span data-stu-id="f5802-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="f5802-129">-工作區</span><span class="sxs-lookup"><span data-stu-id="f5802-129">-Workspace</span></span>
<span data-ttu-id="f5802-130">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="f5802-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f5802-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5802-131">-WorkspaceName</span></span>
<span data-ttu-id="f5802-132">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="f5802-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f5802-133">-確認</span><span class="sxs-lookup"><span data-stu-id="f5802-133">-Confirm</span></span>
<span data-ttu-id="f5802-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5802-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5802-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5802-135">-WhatIf</span></span>
<span data-ttu-id="f5802-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5802-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5802-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5802-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5802-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5802-138">CommonParameters</span></span>
<span data-ttu-id="f5802-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5802-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5802-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5802-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5802-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f5802-141">INPUTS</span></span>

### <span data-ttu-id="f5802-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="f5802-142">PSWorkspace</span></span>
<span data-ttu-id="f5802-143">形參 "Workspace" 接受管線中類型 ' PSWorkspace」的值</span><span class="sxs-lookup"><span data-stu-id="f5802-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="f5802-144">輸出</span><span class="sxs-lookup"><span data-stu-id="f5802-144">OUTPUTS</span></span>

### <span data-ttu-id="f5802-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f5802-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f5802-146">筆記</span><span class="sxs-lookup"><span data-stu-id="f5802-146">NOTES</span></span>

## <span data-ttu-id="f5802-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5802-147">RELATED LINKS</span></span>

