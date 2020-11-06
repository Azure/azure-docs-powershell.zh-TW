---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 07b541636229d65a092dc9a3067d3a4cef89cac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454199"
---
# <span data-ttu-id="d36d2-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="d36d2-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="d36d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d36d2-102">SYNOPSIS</span></span>
<span data-ttu-id="d36d2-103">在收集資料時，無法改善 AzurePowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d36d2-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="d36d2-104">除非您明確加入宣告，否則不會收集資料。</span><span class="sxs-lookup"><span data-stu-id="d36d2-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d36d2-105">句法</span><span class="sxs-lookup"><span data-stu-id="d36d2-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d36d2-106">說明</span><span class="sxs-lookup"><span data-stu-id="d36d2-106">DESCRIPTION</span></span>
<span data-ttu-id="d36d2-107">您可以透過加入宣告資料收集來改善使用 Microsoft 雲端和 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="d36d2-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="d36d2-108">Azure PowerShell 不會在未經您同意的情況下收集資料，您必須在第一次執行 Cmdlet 時，在 Azure PowerShell 提示您 AzureRmDataCollection 收集資料時，再回答 [是]。</span><span class="sxs-lookup"><span data-stu-id="d36d2-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="d36d2-109">Microsoft 匯總收集的資料，以識別使用方式、找出常見問題，以及改善使用 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="d36d2-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="d36d2-110">Microsoft Azure PowerShell 不會收集任何私人資料，或任何個人的可識別資訊。</span><span class="sxs-lookup"><span data-stu-id="d36d2-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="d36d2-111">執行 Disable-AzureRMDataCollection Cmdlet 來停用目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="d36d2-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="d36d2-112">這可防止目前的使用者在第一次執行 Cmdlet 時收到關於資料收集的提示。</span><span class="sxs-lookup"><span data-stu-id="d36d2-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="d36d2-113">若要為目前的使用者啟用資料收集，請執行 Enable-AzureRmDataCollection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d36d2-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="d36d2-114">示例</span><span class="sxs-lookup"><span data-stu-id="d36d2-114">EXAMPLES</span></span>

### <span data-ttu-id="d36d2-115">範例1：停用目前使用者的資料收集</span><span class="sxs-lookup"><span data-stu-id="d36d2-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="d36d2-116">這個範例示範如何停用目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="d36d2-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="d36d2-117">參數</span><span class="sxs-lookup"><span data-stu-id="d36d2-117">PARAMETERS</span></span>

### <span data-ttu-id="d36d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36d2-118">-DefaultProfile</span></span>
<span data-ttu-id="d36d2-119">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="d36d2-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36d2-120">-確認</span><span class="sxs-lookup"><span data-stu-id="d36d2-120">-Confirm</span></span>
<span data-ttu-id="d36d2-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d36d2-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36d2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d36d2-122">-WhatIf</span></span>
<span data-ttu-id="d36d2-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d36d2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d36d2-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d36d2-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d36d2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36d2-125">CommonParameters</span></span>
<span data-ttu-id="d36d2-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d36d2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36d2-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d36d2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36d2-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d36d2-128">INPUTS</span></span>

### <span data-ttu-id="d36d2-129">所有</span><span class="sxs-lookup"><span data-stu-id="d36d2-129">None</span></span>
<span data-ttu-id="d36d2-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d36d2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d36d2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d36d2-131">OUTPUTS</span></span>

### <span data-ttu-id="d36d2-132">所有</span><span class="sxs-lookup"><span data-stu-id="d36d2-132">None</span></span>

## <span data-ttu-id="d36d2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d36d2-133">NOTES</span></span>

## <span data-ttu-id="d36d2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d36d2-134">RELATED LINKS</span></span>

[<span data-ttu-id="d36d2-135">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="d36d2-135">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

