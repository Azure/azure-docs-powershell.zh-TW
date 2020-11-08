---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: 04097dc54bd013e481064678e20bcf9ed559ab0c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137926"
---
# <span data-ttu-id="131ab-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="131ab-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="131ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="131ab-102">SYNOPSIS</span></span>
<span data-ttu-id="131ab-103">在目前登入的環境中重新開機 Analysis Services 伺服器的實例，如 Add-AzAnalysisServicesAccount 命令中所指定</span><span class="sxs-lookup"><span data-stu-id="131ab-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="131ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="131ab-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="131ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="131ab-105">DESCRIPTION</span></span>
<span data-ttu-id="131ab-106">Restart-AzAnalysisServicesInstance Cmdlet 會重新開機 Azure Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="131ab-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="131ab-107">示例</span><span class="sxs-lookup"><span data-stu-id="131ab-107">EXAMPLES</span></span>

### <span data-ttu-id="131ab-108">範例1</span><span class="sxs-lookup"><span data-stu-id="131ab-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="131ab-109">這個命令會在 Add-AzAnalysisServicesAccount 命令中指定的環境中，重新開機伺服器「testserver」</span><span class="sxs-lookup"><span data-stu-id="131ab-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="131ab-110">參數</span><span class="sxs-lookup"><span data-stu-id="131ab-110">PARAMETERS</span></span>

### <span data-ttu-id="131ab-111">-實例</span><span class="sxs-lookup"><span data-stu-id="131ab-111">-Instance</span></span>
<span data-ttu-id="131ab-112">要重新開機之 Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="131ab-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="131ab-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="131ab-113">-PassThru</span></span>
<span data-ttu-id="131ab-114">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="131ab-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="131ab-115">-確認</span><span class="sxs-lookup"><span data-stu-id="131ab-115">-Confirm</span></span>
<span data-ttu-id="131ab-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="131ab-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131ab-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131ab-117">-WhatIf</span></span>
<span data-ttu-id="131ab-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="131ab-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131ab-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="131ab-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131ab-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131ab-120">CommonParameters</span></span>
<span data-ttu-id="131ab-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="131ab-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131ab-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="131ab-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131ab-123">輸入</span><span class="sxs-lookup"><span data-stu-id="131ab-123">INPUTS</span></span>

### <span data-ttu-id="131ab-124">所有</span><span class="sxs-lookup"><span data-stu-id="131ab-124">None</span></span>

## <span data-ttu-id="131ab-125">輸出</span><span class="sxs-lookup"><span data-stu-id="131ab-125">OUTPUTS</span></span>

### <span data-ttu-id="131ab-126">System.object</span><span class="sxs-lookup"><span data-stu-id="131ab-126">System.Boolean</span></span>

## <span data-ttu-id="131ab-127">筆記</span><span class="sxs-lookup"><span data-stu-id="131ab-127">NOTES</span></span>
<span data-ttu-id="131ab-128">別名： Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="131ab-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="131ab-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="131ab-129">RELATED LINKS</span></span>