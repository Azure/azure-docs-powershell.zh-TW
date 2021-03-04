---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: c5ffd95cb3bd5e902e2e9edadfa9c96dd441c744
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903729"
---
# <span data-ttu-id="00805-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="00805-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="00805-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00805-102">SYNOPSIS</span></span>

<span data-ttu-id="00805-103">將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理至目前登入環境的所有查詢縮放實例，Add-AzAnalysisServicesAccount命令</span><span class="sxs-lookup"><span data-stu-id="00805-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="00805-104">語法</span><span class="sxs-lookup"><span data-stu-id="00805-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00805-105">描述</span><span class="sxs-lookup"><span data-stu-id="00805-105">DESCRIPTION</span></span>

<span data-ttu-id="00805-106">此Sync-AzAnalysisServicesInstance Cmdlet 會按照 Add-AzAnalysisServicesAccount 命令，將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理至目前登入環境中的所有查詢縮放實例</span><span class="sxs-lookup"><span data-stu-id="00805-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="00805-107">例子</span><span class="sxs-lookup"><span data-stu-id="00805-107">EXAMPLES</span></span>

### <span data-ttu-id="00805-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="00805-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="00805-109">此命令會同步處理環境中名為 "contoso" 之伺服器中名為 SalesOrders 的資料庫westus.asazure.windows.net只要使用者已使用 Add-AzAnalysisServicesAccount 命令登入此環境。</span><span class="sxs-lookup"><span data-stu-id="00805-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="00805-110">參數</span><span class="sxs-lookup"><span data-stu-id="00805-110">PARAMETERS</span></span>

### <span data-ttu-id="00805-111">-資料庫</span><span class="sxs-lookup"><span data-stu-id="00805-111">-Database</span></span>

<span data-ttu-id="00805-112">要同步的資料庫身分識別</span><span class="sxs-lookup"><span data-stu-id="00805-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="00805-113">-實例</span><span class="sxs-lookup"><span data-stu-id="00805-113">-Instance</span></span>

<span data-ttu-id="00805-114">要重新開機的 Analysis Services 伺服器實例名稱</span><span class="sxs-lookup"><span data-stu-id="00805-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="00805-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00805-115">-PassThru</span></span>

<span data-ttu-id="00805-116">如果命令成功，指定此選項會返回 True。</span><span class="sxs-lookup"><span data-stu-id="00805-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="00805-117">-確認</span><span class="sxs-lookup"><span data-stu-id="00805-117">-Confirm</span></span>
<span data-ttu-id="00805-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="00805-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00805-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00805-119">-WhatIf</span></span>
<span data-ttu-id="00805-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00805-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00805-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00805-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00805-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00805-122">CommonParameters</span></span>
<span data-ttu-id="00805-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00805-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00805-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="00805-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00805-125">輸入</span><span class="sxs-lookup"><span data-stu-id="00805-125">INPUTS</span></span>

### <span data-ttu-id="00805-126">System.String</span><span class="sxs-lookup"><span data-stu-id="00805-126">System.String</span></span>

## <span data-ttu-id="00805-127">輸出</span><span class="sxs-lookup"><span data-stu-id="00805-127">OUTPUTS</span></span>

### <span data-ttu-id="00805-128">Microsoft.Azure.Commands.AnalysisServices.Dataservices.Dataservice.models.ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="00805-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="00805-129">筆記</span><span class="sxs-lookup"><span data-stu-id="00805-129">NOTES</span></span>

<span data-ttu-id="00805-130">別名：Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="00805-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="00805-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="00805-131">RELATED LINKS</span></span>
