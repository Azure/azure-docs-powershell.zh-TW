---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614207"
---
# <span data-ttu-id="f6611-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f6611-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="f6611-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6611-102">SYNOPSIS</span></span>
<span data-ttu-id="f6611-103">啟用 Azure PowerShell 以收集資料，以使用 AzurePowerShell Cmdlet 來改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="f6611-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="f6611-104">執行此 Cmdlet 會將您的目前使用者的資料收集加入到目前的電腦上。</span><span class="sxs-lookup"><span data-stu-id="f6611-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="f6611-105">除非您明確加入宣告，否則不會收集任何資料。</span><span class="sxs-lookup"><span data-stu-id="f6611-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="f6611-106">句法</span><span class="sxs-lookup"><span data-stu-id="f6611-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6611-107">說明</span><span class="sxs-lookup"><span data-stu-id="f6611-107">DESCRIPTION</span></span>
<span data-ttu-id="f6611-108">您可以透過加入宣告資料收集來改善使用 Microsoft 雲端和 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="f6611-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="f6611-109">Azure PowerShell 不會在未經您同意的情況下收集資料，您必須在第一次執行 Cmdlet 時，在 Azure PowerShell 提示您 AzDataCollection 收集資料時，再回答 [是]。</span><span class="sxs-lookup"><span data-stu-id="f6611-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="f6611-110">Microsoft 匯總收集的資料，以識別使用方式、找出常見問題，以及改善使用 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="f6611-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="f6611-111">Microsoft Azure PowerShell 不會收集任何私人資料，或任何個人的可識別資訊。</span><span class="sxs-lookup"><span data-stu-id="f6611-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="f6611-112">執行 Enable-AzDataCollection Cmdlet，在目前的電腦上啟用目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="f6611-112">Run the Enable-AzDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="f6611-113">這可防止目前的使用者在第一次執行 Cmdlet 時收到關於資料收集的提示。</span><span class="sxs-lookup"><span data-stu-id="f6611-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="f6611-114">若要停用目前使用者的資料收集，請執行 Disable-AzDataCollection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6611-114">To disable data collection for the current user, run the Disable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="f6611-115">示例</span><span class="sxs-lookup"><span data-stu-id="f6611-115">EXAMPLES</span></span>

### <span data-ttu-id="f6611-116">範例1：為目前的使用者啟用資料收集</span><span class="sxs-lookup"><span data-stu-id="f6611-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzDataCollection
```

<span data-ttu-id="f6611-117">此範例說明如何為目前的使用者啟用資料收集。</span><span class="sxs-lookup"><span data-stu-id="f6611-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="f6611-118">參數</span><span class="sxs-lookup"><span data-stu-id="f6611-118">PARAMETERS</span></span>

### <span data-ttu-id="f6611-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6611-119">-DefaultProfile</span></span>
<span data-ttu-id="f6611-120">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6611-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6611-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f6611-121">-Confirm</span></span>
<span data-ttu-id="f6611-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6611-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6611-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6611-123">-WhatIf</span></span>
<span data-ttu-id="f6611-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6611-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6611-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6611-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6611-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6611-126">CommonParameters</span></span>
<span data-ttu-id="f6611-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6611-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6611-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6611-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6611-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f6611-129">INPUTS</span></span>

### <span data-ttu-id="f6611-130">所有</span><span class="sxs-lookup"><span data-stu-id="f6611-130">None</span></span>

## <span data-ttu-id="f6611-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f6611-131">OUTPUTS</span></span>

### <span data-ttu-id="f6611-132">System.void</span><span class="sxs-lookup"><span data-stu-id="f6611-132">System.Void</span></span>

## <span data-ttu-id="f6611-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f6611-133">NOTES</span></span>

## <span data-ttu-id="f6611-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6611-134">RELATED LINKS</span></span>

[<span data-ttu-id="f6611-135">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f6611-135">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)

