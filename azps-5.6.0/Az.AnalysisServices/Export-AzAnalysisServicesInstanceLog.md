---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/export-azanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Export-AzAnalysisServicesInstanceLog.md
ms.openlocfilehash: 3e4e3b2c2f90420f198d2900d5de0d519ffde81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917809"
---
# <span data-ttu-id="aeca9-101">Export-AzAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="aeca9-101">Export-AzAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="aeca9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aeca9-102">SYNOPSIS</span></span>
<span data-ttu-id="aeca9-103">從目前登入環境的分析服務伺服器實例匯出記錄，Add-AzAnalysisServicesAccount命令</span><span class="sxs-lookup"><span data-stu-id="aeca9-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="aeca9-104">語法</span><span class="sxs-lookup"><span data-stu-id="aeca9-104">SYNTAX</span></span>

```
Export-AzAnalysisServicesInstanceLog -OutputPath <String> [-Force] [-Instance] <String> [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeca9-105">描述</span><span class="sxs-lookup"><span data-stu-id="aeca9-105">DESCRIPTION</span></span>
<span data-ttu-id="aeca9-106">Cmdlet Export-AzAnalysisServicesInstance Azure Analysis Services 伺服器實例匯出記錄至檔案</span><span class="sxs-lookup"><span data-stu-id="aeca9-106">The Export-AzAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="aeca9-107">例子</span><span class="sxs-lookup"><span data-stu-id="aeca9-107">EXAMPLES</span></span>

### <span data-ttu-id="aeca9-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="aeca9-108">Example 1</span></span>
```
PS C:\>Export-AzAnalysisServicesInstanceLog -Instance testserver -OutputPath C:\path\to\log\testserver.log
```

<span data-ttu-id="aeca9-109">此命令會從 Add-AzAnalysisServicesAccount 命令所指定的環境中，從伺服器 'testserver' 匯出記錄，並將其儲存到 OutputPath 'C：\path\to\log\testserver.log' 中指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="aeca9-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="aeca9-110">參數</span><span class="sxs-lookup"><span data-stu-id="aeca9-110">PARAMETERS</span></span>

### <span data-ttu-id="aeca9-111">-強制</span><span class="sxs-lookup"><span data-stu-id="aeca9-111">-Force</span></span>
<span data-ttu-id="aeca9-112">覆寫檔案</span><span class="sxs-lookup"><span data-stu-id="aeca9-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="aeca9-113">-實例</span><span class="sxs-lookup"><span data-stu-id="aeca9-113">-Instance</span></span>
<span data-ttu-id="aeca9-114">Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="aeca9-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="aeca9-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="aeca9-115">-OutputPath</span></span>
<span data-ttu-id="aeca9-116">匯出記錄檔案的輸出路徑</span><span class="sxs-lookup"><span data-stu-id="aeca9-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="aeca9-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aeca9-117">-PassThru</span></span>
<span data-ttu-id="aeca9-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="aeca9-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="aeca9-119">-確認</span><span class="sxs-lookup"><span data-stu-id="aeca9-119">-Confirm</span></span>
<span data-ttu-id="aeca9-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="aeca9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeca9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeca9-121">-WhatIf</span></span>
<span data-ttu-id="aeca9-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aeca9-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeca9-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aeca9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeca9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeca9-124">CommonParameters</span></span>
<span data-ttu-id="aeca9-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aeca9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeca9-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="aeca9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeca9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="aeca9-127">INPUTS</span></span>

### <span data-ttu-id="aeca9-128">沒有</span><span class="sxs-lookup"><span data-stu-id="aeca9-128">None</span></span>

## <span data-ttu-id="aeca9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="aeca9-129">OUTPUTS</span></span>

### <span data-ttu-id="aeca9-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="aeca9-130">System.Void</span></span>

## <span data-ttu-id="aeca9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="aeca9-131">NOTES</span></span>
<span data-ttu-id="aeca9-132">別名：Export-AzAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="aeca9-132">Alias: Export-AzAsInstanceLog</span></span>

## <span data-ttu-id="aeca9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="aeca9-133">RELATED LINKS</span></span>
