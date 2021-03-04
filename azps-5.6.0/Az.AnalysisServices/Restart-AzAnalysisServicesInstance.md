---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/restart-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Restart-AzAnalysisServicesInstance.md
ms.openlocfilehash: b0bb5d90fe304d2663671fdc8a2277d2adb18322
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907913"
---
# <span data-ttu-id="a32ff-101">Restart-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="a32ff-101">Restart-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="a32ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a32ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a32ff-103">重新開機目前登入環境中 Analysis Services 伺服器的實例，Add-AzAnalysisServicesAccount命令</span><span class="sxs-lookup"><span data-stu-id="a32ff-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="a32ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="a32ff-104">SYNTAX</span></span>

```
Restart-AzAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a32ff-105">描述</span><span class="sxs-lookup"><span data-stu-id="a32ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a32ff-106">Cmdlet Restart-AzAnalysisServicesInstance Azure Analysis Services 伺服器實例重新開機</span><span class="sxs-lookup"><span data-stu-id="a32ff-106">The Restart-AzAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="a32ff-107">例子</span><span class="sxs-lookup"><span data-stu-id="a32ff-107">EXAMPLES</span></span>

### <span data-ttu-id="a32ff-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="a32ff-108">Example 1</span></span>
```
PS C:\>Restart-AzAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="a32ff-109">此命令會重新開機伺服器在 Add-AzAnalysisServicesAccount 命令中指定的環境</span><span class="sxs-lookup"><span data-stu-id="a32ff-109">This command will restart the server 'testserver' in the environment specified in the Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="a32ff-110">參數</span><span class="sxs-lookup"><span data-stu-id="a32ff-110">PARAMETERS</span></span>

### <span data-ttu-id="a32ff-111">-實例</span><span class="sxs-lookup"><span data-stu-id="a32ff-111">-Instance</span></span>
<span data-ttu-id="a32ff-112">要重新開機的 Analysis Services 伺服器實例名稱</span><span class="sxs-lookup"><span data-stu-id="a32ff-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="a32ff-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a32ff-113">-PassThru</span></span>
<span data-ttu-id="a32ff-114">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="a32ff-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a32ff-115">-確認</span><span class="sxs-lookup"><span data-stu-id="a32ff-115">-Confirm</span></span>
<span data-ttu-id="a32ff-116">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a32ff-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32ff-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32ff-117">-WhatIf</span></span>
<span data-ttu-id="a32ff-118">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a32ff-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a32ff-119">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a32ff-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32ff-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32ff-120">CommonParameters</span></span>
<span data-ttu-id="a32ff-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a32ff-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32ff-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a32ff-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32ff-123">輸入</span><span class="sxs-lookup"><span data-stu-id="a32ff-123">INPUTS</span></span>

### <span data-ttu-id="a32ff-124">沒有</span><span class="sxs-lookup"><span data-stu-id="a32ff-124">None</span></span>

## <span data-ttu-id="a32ff-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a32ff-125">OUTPUTS</span></span>

### <span data-ttu-id="a32ff-126">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a32ff-126">System.Boolean</span></span>

## <span data-ttu-id="a32ff-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a32ff-127">NOTES</span></span>
<span data-ttu-id="a32ff-128">別名：Restart-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="a32ff-128">Alias: Restart-AzAsInstance</span></span>

## <span data-ttu-id="a32ff-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a32ff-129">RELATED LINKS</span></span>
