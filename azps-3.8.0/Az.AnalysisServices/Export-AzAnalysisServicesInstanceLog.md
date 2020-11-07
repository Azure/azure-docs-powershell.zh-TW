---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 57fe2159ab53e1a822da376a07546202ac672cb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957127"
---
# <span data-ttu-id="e8bd9-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="e8bd9-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="e8bd9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8bd9-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bd9-103">根據 Add-AzAnalysisServicesAccount 命令中指定的，從目前登入的環境中的 Analysis Services 伺服器實例匯出記錄</span><span class="sxs-lookup"><span data-stu-id="e8bd9-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="e8bd9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8bd9-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8bd9-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8bd9-105">DESCRIPTION</span></span>
<span data-ttu-id="e8bd9-106">Export-AzAnalysisServicesInstance Cmdlet 會將來自 Azure Analysis Services 伺服器實例的記錄匯出至檔案</span><span class="sxs-lookup"><span data-stu-id="e8bd9-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="e8bd9-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8bd9-107">EXAMPLES</span></span>

### <span data-ttu-id="e8bd9-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e8bd9-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="e8bd9-109">這個命令會從 [Add-AzAnalysisServicesAccount] 命令指定之環境中的伺服器 ' testserver」匯出記錄，並將其儲存到 OutputPath ' C:\path\to\log\testserver.log」中指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="e8bd9-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="e8bd9-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8bd9-110">PARAMETERS</span></span>

### <span data-ttu-id="e8bd9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e8bd9-111">-Force</span></span>
<span data-ttu-id="e8bd9-112">覆蓋檔案（如果有的話）而不詢問</span><span class="sxs-lookup"><span data-stu-id="e8bd9-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="e8bd9-113">-實例</span><span class="sxs-lookup"><span data-stu-id="e8bd9-113">-Instance</span></span>
<span data-ttu-id="e8bd9-114">Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="e8bd9-114">Name of the Analysis Services server instance</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd9-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="e8bd9-115">-OutputPath</span></span>
<span data-ttu-id="e8bd9-116">匯出記錄至檔案的輸出路徑</span><span class="sxs-lookup"><span data-stu-id="e8bd9-116">Output path to file to export log</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8bd9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8bd9-117">-PassThru</span></span>
<span data-ttu-id="e8bd9-118">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="e8bd9-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e8bd9-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e8bd9-119">-Confirm</span></span>
<span data-ttu-id="e8bd9-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8bd9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8bd9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8bd9-121">-WhatIf</span></span>
<span data-ttu-id="e8bd9-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8bd9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8bd9-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8bd9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8bd9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bd9-124">CommonParameters</span></span>
<span data-ttu-id="e8bd9-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8bd9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bd9-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8bd9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bd9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e8bd9-127">INPUTS</span></span>

### <span data-ttu-id="e8bd9-128">所有</span><span class="sxs-lookup"><span data-stu-id="e8bd9-128">None</span></span>

## <span data-ttu-id="e8bd9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e8bd9-129">OUTPUTS</span></span>

### <span data-ttu-id="e8bd9-130">System.void</span><span class="sxs-lookup"><span data-stu-id="e8bd9-130">System.Void</span></span>

## <span data-ttu-id="e8bd9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e8bd9-131">NOTES</span></span>
<span data-ttu-id="e8bd9-132">別名： Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="e8bd9-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="e8bd9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8bd9-133">RELATED LINKS</span></span>
