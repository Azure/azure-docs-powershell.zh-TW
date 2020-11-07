---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 185b152d3fe4ac4cb7d80acb6d33c408911d626d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959825"
---
# <span data-ttu-id="06298-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="06298-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="06298-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06298-102">SYNOPSIS</span></span>

<span data-ttu-id="06298-103">將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前登入的 scaleout 中的所有查詢實例，如 Add-AzAnalysisServicesAccount 命令中所指定</span><span class="sxs-lookup"><span data-stu-id="06298-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="06298-104">句法</span><span class="sxs-lookup"><span data-stu-id="06298-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06298-105">說明</span><span class="sxs-lookup"><span data-stu-id="06298-105">DESCRIPTION</span></span>

<span data-ttu-id="06298-106">Sync-AzAnalysisServicesInstance Cmdlet 會將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前已登入的 [Add-AzAnalysisServicesAccount] 命令中指定的所有查詢 scaleout 實例</span><span class="sxs-lookup"><span data-stu-id="06298-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="06298-107">示例</span><span class="sxs-lookup"><span data-stu-id="06298-107">EXAMPLES</span></span>

### <span data-ttu-id="06298-108">範例1</span><span class="sxs-lookup"><span data-stu-id="06298-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="06298-109">這個命令會在環境 westus.asazure.windows.net 中，同步處理名為「contoso」的伺服器中名為 SalesOrders 的資料庫，前提是使用者已使用 Add-AzAnalysisServicesAccount 命令登入這個環境。</span><span class="sxs-lookup"><span data-stu-id="06298-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="06298-110">參數</span><span class="sxs-lookup"><span data-stu-id="06298-110">PARAMETERS</span></span>

### <span data-ttu-id="06298-111">-資料庫</span><span class="sxs-lookup"><span data-stu-id="06298-111">-Database</span></span>

<span data-ttu-id="06298-112">要同步處理的資料庫身分識別</span><span class="sxs-lookup"><span data-stu-id="06298-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06298-113">-實例</span><span class="sxs-lookup"><span data-stu-id="06298-113">-Instance</span></span>

<span data-ttu-id="06298-114">要重新開機之 Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="06298-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="06298-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06298-115">-PassThru</span></span>

<span data-ttu-id="06298-116">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="06298-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="06298-117">-確認</span><span class="sxs-lookup"><span data-stu-id="06298-117">-Confirm</span></span>
<span data-ttu-id="06298-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="06298-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06298-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06298-119">-WhatIf</span></span>
<span data-ttu-id="06298-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06298-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06298-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06298-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06298-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06298-122">CommonParameters</span></span>
<span data-ttu-id="06298-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06298-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06298-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06298-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06298-125">輸入</span><span class="sxs-lookup"><span data-stu-id="06298-125">INPUTS</span></span>

### <span data-ttu-id="06298-126">System.object</span><span class="sxs-lookup"><span data-stu-id="06298-126">System.String</span></span>

## <span data-ttu-id="06298-127">輸出</span><span class="sxs-lookup"><span data-stu-id="06298-127">OUTPUTS</span></span>

### <span data-ttu-id="06298-128">Dataplane. ScaleOutServerDatabaseSyncDetails （AnalysisServices）</span><span class="sxs-lookup"><span data-stu-id="06298-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="06298-129">筆記</span><span class="sxs-lookup"><span data-stu-id="06298-129">NOTES</span></span>

<span data-ttu-id="06298-130">別名： Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="06298-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="06298-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="06298-131">RELATED LINKS</span></span>
