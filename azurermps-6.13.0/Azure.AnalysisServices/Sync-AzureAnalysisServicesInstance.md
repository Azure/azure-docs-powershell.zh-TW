---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: 732eb92a46fa7e69ba5274398de648c16142ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445880"
---
# <span data-ttu-id="45a21-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="45a21-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="45a21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45a21-102">SYNOPSIS</span></span>

<span data-ttu-id="45a21-103">將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前登入的 scaleout 中的所有查詢實例，如 Add-AzureAnalysisServicesAccount 命令中所指定</span><span class="sxs-lookup"><span data-stu-id="45a21-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a21-104">句法</span><span class="sxs-lookup"><span data-stu-id="45a21-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45a21-105">說明</span><span class="sxs-lookup"><span data-stu-id="45a21-105">DESCRIPTION</span></span>

<span data-ttu-id="45a21-106">Sync-AzureAnalysisServicesInstance Cmdlet 會將指定的 Analysis Services 伺服器實例上的指定資料庫同步處理到目前已登入的 [Add-AzureAnalysisServicesAccount] 命令中指定的所有查詢 scaleout 實例</span><span class="sxs-lookup"><span data-stu-id="45a21-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="45a21-107">示例</span><span class="sxs-lookup"><span data-stu-id="45a21-107">EXAMPLES</span></span>

### <span data-ttu-id="45a21-108">範例1</span><span class="sxs-lookup"><span data-stu-id="45a21-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="45a21-109">這個命令會在環境 westus.asazure.windows.net 中，同步處理名為「contoso」的伺服器中名為 SalesOrders 的資料庫，前提是使用者已使用 Add-AzureAnalysisServicesAccount 命令登入此環境。</span><span class="sxs-lookup"><span data-stu-id="45a21-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="45a21-110">參數</span><span class="sxs-lookup"><span data-stu-id="45a21-110">PARAMETERS</span></span>

### <span data-ttu-id="45a21-111">-資料庫</span><span class="sxs-lookup"><span data-stu-id="45a21-111">-Database</span></span>

<span data-ttu-id="45a21-112">要同步處理的資料庫身分識別</span><span class="sxs-lookup"><span data-stu-id="45a21-112">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="45a21-113">-實例</span><span class="sxs-lookup"><span data-stu-id="45a21-113">-Instance</span></span>

<span data-ttu-id="45a21-114">要重新開機之 Analysis Services 伺服器實例的名稱</span><span class="sxs-lookup"><span data-stu-id="45a21-114">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="45a21-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45a21-115">-PassThru</span></span>

<span data-ttu-id="45a21-116">如果命令成功，則指定此值會傳回 true。</span><span class="sxs-lookup"><span data-stu-id="45a21-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="45a21-117">-確認</span><span class="sxs-lookup"><span data-stu-id="45a21-117">-Confirm</span></span>
<span data-ttu-id="45a21-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="45a21-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45a21-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45a21-119">-WhatIf</span></span>
<span data-ttu-id="45a21-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45a21-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45a21-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45a21-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45a21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a21-122">CommonParameters</span></span>
<span data-ttu-id="45a21-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45a21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a21-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45a21-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a21-125">輸入</span><span class="sxs-lookup"><span data-stu-id="45a21-125">INPUTS</span></span>

### <span data-ttu-id="45a21-126">System.object</span><span class="sxs-lookup"><span data-stu-id="45a21-126">System.String</span></span>
<span data-ttu-id="45a21-127">參數： Database (ByValue) 、Instance (ByValue) </span><span class="sxs-lookup"><span data-stu-id="45a21-127">Parameters: Database (ByValue), Instance (ByValue)</span></span>

## <span data-ttu-id="45a21-128">輸出</span><span class="sxs-lookup"><span data-stu-id="45a21-128">OUTPUTS</span></span>

### <span data-ttu-id="45a21-129">Dataplane. ScaleOutServerDatabaseSyncDetails （AnalysisServices）</span><span class="sxs-lookup"><span data-stu-id="45a21-129">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="45a21-130">筆記</span><span class="sxs-lookup"><span data-stu-id="45a21-130">NOTES</span></span>

<span data-ttu-id="45a21-131">別名： Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="45a21-131">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="45a21-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="45a21-132">RELATED LINKS</span></span>
