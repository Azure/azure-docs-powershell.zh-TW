---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/export-azureanalysisservicesinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: dad0e14b72c256706456ed3c923b966323fd7dad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447549"
---
# <span data-ttu-id="803af-101">Export-AzureAnalysisServicesInstanceLog</span><span class="sxs-lookup"><span data-stu-id="803af-101">Export-AzureAnalysisServicesInstanceLog</span></span>

## <span data-ttu-id="803af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="803af-102">SYNOPSIS</span></span>
<span data-ttu-id="803af-103">根據 Add-AzureAnalysisServicesAccount 命令中指定的，從目前登入的環境中的 Analysis Services 伺服器實例匯出記錄</span><span class="sxs-lookup"><span data-stu-id="803af-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="803af-104">句法</span><span class="sxs-lookup"><span data-stu-id="803af-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog -Instance <String> -OutputPath <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="803af-105">說明</span><span class="sxs-lookup"><span data-stu-id="803af-105">DESCRIPTION</span></span>
<span data-ttu-id="803af-106">Export-AzureAnalysisServicesInstance Cmdlet 會將來自 Azure Analysis Services 伺服器實例的記錄匯出至檔案</span><span class="sxs-lookup"><span data-stu-id="803af-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="803af-107">示例</span><span class="sxs-lookup"><span data-stu-id="803af-107">EXAMPLES</span></span>

### <span data-ttu-id="803af-108">範例1</span><span class="sxs-lookup"><span data-stu-id="803af-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="803af-109">這個命令會從 [Add-AzureAnalysisServicesAccount] 命令指定之環境中的伺服器 ' testserver」匯出記錄，並將其儲存到 OutputPath ' C:\path\to\log\testserver.log」中指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="803af-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="803af-110">參數</span><span class="sxs-lookup"><span data-stu-id="803af-110">PARAMETERS</span></span>

### <span data-ttu-id="803af-111">-Force</span><span class="sxs-lookup"><span data-stu-id="803af-111">-Force</span></span>
<span data-ttu-id="803af-112">覆蓋檔案（如果有的話）而不詢問</span><span class="sxs-lookup"><span data-stu-id="803af-112">Overwrite file if exists without asking</span></span>

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

### <span data-ttu-id="803af-113">-實例</span><span class="sxs-lookup"><span data-stu-id="803af-113">-Instance</span></span>
<span data-ttu-id="803af-114">Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="803af-114">Name of the Analysis Services server instance</span></span>

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

### <span data-ttu-id="803af-115">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="803af-115">-OutputPath</span></span>
<span data-ttu-id="803af-116">匯出記錄至檔案的輸出路徑</span><span class="sxs-lookup"><span data-stu-id="803af-116">Output path to file to export log</span></span>

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

### <span data-ttu-id="803af-117">-確認</span><span class="sxs-lookup"><span data-stu-id="803af-117">-Confirm</span></span>
<span data-ttu-id="803af-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="803af-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="803af-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="803af-119">-WhatIf</span></span>
<span data-ttu-id="803af-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="803af-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="803af-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="803af-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="803af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803af-122">CommonParameters</span></span>
<span data-ttu-id="803af-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="803af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803af-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="803af-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803af-125">輸入</span><span class="sxs-lookup"><span data-stu-id="803af-125">INPUTS</span></span>

### <span data-ttu-id="803af-126">所有</span><span class="sxs-lookup"><span data-stu-id="803af-126">None</span></span>

## <span data-ttu-id="803af-127">輸出</span><span class="sxs-lookup"><span data-stu-id="803af-127">OUTPUTS</span></span>

### <span data-ttu-id="803af-128">System.void</span><span class="sxs-lookup"><span data-stu-id="803af-128">System.Void</span></span>

## <span data-ttu-id="803af-129">筆記</span><span class="sxs-lookup"><span data-stu-id="803af-129">NOTES</span></span>
<span data-ttu-id="803af-130">別名： Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="803af-130">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="803af-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="803af-131">RELATED LINKS</span></span>
