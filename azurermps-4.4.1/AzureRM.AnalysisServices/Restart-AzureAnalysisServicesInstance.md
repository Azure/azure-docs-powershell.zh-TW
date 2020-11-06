---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Restart-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 038c7456f849777f16ca0113d799b4ee8a16cd2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445239"
---
# <span data-ttu-id="131c4-101">Restart-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="131c4-101">Restart-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="131c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="131c4-102">SYNOPSIS</span></span>
<span data-ttu-id="131c4-103">在目前登入的環境中重新開機 Analysis Services 伺服器的實例，如 Add-AzureAnalysisServicesAccount 命令中所指定</span><span class="sxs-lookup"><span data-stu-id="131c4-103">Restarts an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="131c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="131c4-104">SYNTAX</span></span>

```
Restart-AzureAnalysisServicesInstance [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="131c4-105">說明</span><span class="sxs-lookup"><span data-stu-id="131c4-105">DESCRIPTION</span></span>
<span data-ttu-id="131c4-106">Restart-AzureAnalysisServicesInstance Cmdlet 會重新開機 Azure Analysis Services 伺服器的實例</span><span class="sxs-lookup"><span data-stu-id="131c4-106">The Restart-AzureAnalysisServicesInstance cmdlet restarts an instance of Azure Analysis Services server</span></span>

## <span data-ttu-id="131c4-107">示例</span><span class="sxs-lookup"><span data-stu-id="131c4-107">EXAMPLES</span></span>

### <span data-ttu-id="131c4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="131c4-108">Example 1</span></span>
```
PS C:\>Restart-AzureAnalysisServicesInstance
Instance: testserver
```

<span data-ttu-id="131c4-109">這個命令會在 Add-AzureAnalysisServicesAccount 命令中指定的環境中，重新開機伺服器「testserver」</span><span class="sxs-lookup"><span data-stu-id="131c4-109">This command will restart the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="131c4-110">參數</span><span class="sxs-lookup"><span data-stu-id="131c4-110">PARAMETERS</span></span>

### <span data-ttu-id="131c4-111">-實例</span><span class="sxs-lookup"><span data-stu-id="131c4-111">-Instance</span></span>
<span data-ttu-id="131c4-112">要重新開機之 Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="131c4-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="131c4-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="131c4-113">-PassThru</span></span>
<span data-ttu-id="131c4-114">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="131c4-114">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="131c4-115">-確認</span><span class="sxs-lookup"><span data-stu-id="131c4-115">-Confirm</span></span>
<span data-ttu-id="131c4-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="131c4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131c4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131c4-117">-WhatIf</span></span>
<span data-ttu-id="131c4-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="131c4-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131c4-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="131c4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131c4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131c4-120">CommonParameters</span></span>
<span data-ttu-id="131c4-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="131c4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131c4-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="131c4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131c4-123">輸入</span><span class="sxs-lookup"><span data-stu-id="131c4-123">INPUTS</span></span>

## <span data-ttu-id="131c4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="131c4-124">OUTPUTS</span></span>

### <span data-ttu-id="131c4-125">System.object</span><span class="sxs-lookup"><span data-stu-id="131c4-125">System.Boolean</span></span>

## <span data-ttu-id="131c4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="131c4-126">NOTES</span></span>
<span data-ttu-id="131c4-127">別名： Restart-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="131c4-127">Alias: Restart-AzureAsInstance</span></span>

## <span data-ttu-id="131c4-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="131c4-128">RELATED LINKS</span></span>

