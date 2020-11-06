---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: e78a361bfb332bc2a8bcb226fae946a3abc0a05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614213"
---
# <span data-ttu-id="cdf7b-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="cdf7b-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="cdf7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cdf7b-102">SYNOPSIS</span></span>
<span data-ttu-id="cdf7b-103">在收集資料時，無法改善 AzurePowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="cdf7b-104">除非您明確加入宣告，否則不會收集資料。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="cdf7b-105">句法</span><span class="sxs-lookup"><span data-stu-id="cdf7b-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdf7b-106">說明</span><span class="sxs-lookup"><span data-stu-id="cdf7b-106">DESCRIPTION</span></span>
<span data-ttu-id="cdf7b-107">您可以透過加入宣告資料收集來改善使用 Microsoft 雲端和 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="cdf7b-108">Azure PowerShell 不會在未經您同意的情況下收集資料，您必須在第一次執行 Cmdlet 時，在 Azure PowerShell 提示您 AzDataCollection 收集資料時，再回答 [是]。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="cdf7b-109">Microsoft 匯總收集的資料，以識別使用方式、找出常見問題，以及改善使用 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="cdf7b-110">Microsoft Azure PowerShell 不會收集任何私人資料，或任何個人的可識別資訊。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="cdf7b-111">執行 Disable-AzDataCollection Cmdlet 來停用目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-111">Run the Disable-AzDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="cdf7b-112">這可防止目前的使用者在第一次執行 Cmdlet 時收到關於資料收集的提示。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="cdf7b-113">若要為目前的使用者啟用資料收集，請執行 Enable-AzDataCollection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-113">To enable data collection for the current user, run the Enable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="cdf7b-114">示例</span><span class="sxs-lookup"><span data-stu-id="cdf7b-114">EXAMPLES</span></span>

### <span data-ttu-id="cdf7b-115">範例1：停用目前使用者的資料收集</span><span class="sxs-lookup"><span data-stu-id="cdf7b-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzDataCollection
```

<span data-ttu-id="cdf7b-116">這個範例示範如何停用目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="cdf7b-117">參數</span><span class="sxs-lookup"><span data-stu-id="cdf7b-117">PARAMETERS</span></span>

### <span data-ttu-id="cdf7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdf7b-118">-DefaultProfile</span></span>
<span data-ttu-id="cdf7b-119">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf7b-120">-確認</span><span class="sxs-lookup"><span data-stu-id="cdf7b-120">-Confirm</span></span>
<span data-ttu-id="cdf7b-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf7b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdf7b-122">-WhatIf</span></span>
<span data-ttu-id="cdf7b-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdf7b-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf7b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdf7b-125">CommonParameters</span></span>
<span data-ttu-id="cdf7b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdf7b-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cdf7b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdf7b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="cdf7b-128">INPUTS</span></span>

### <span data-ttu-id="cdf7b-129">所有</span><span class="sxs-lookup"><span data-stu-id="cdf7b-129">None</span></span>

## <span data-ttu-id="cdf7b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cdf7b-130">OUTPUTS</span></span>

### <span data-ttu-id="cdf7b-131">System.void</span><span class="sxs-lookup"><span data-stu-id="cdf7b-131">System.Void</span></span>

## <span data-ttu-id="cdf7b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cdf7b-132">NOTES</span></span>

## <span data-ttu-id="cdf7b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="cdf7b-133">RELATED LINKS</span></span>

[<span data-ttu-id="cdf7b-134">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="cdf7b-134">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

