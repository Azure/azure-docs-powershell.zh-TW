---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 83c7bda6c7b41f857bac9b63afcca07baa6ecd93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455943"
---
# <span data-ttu-id="35b67-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="35b67-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="35b67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35b67-102">SYNOPSIS</span></span>
<span data-ttu-id="35b67-103">啟用 Azure PowerShell 以收集資料，以使用 AzurePowerShell Cmdlet 來改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="35b67-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="35b67-104">執行此 Cmdlet 會將您的目前使用者的資料收集加入到目前的電腦上。</span><span class="sxs-lookup"><span data-stu-id="35b67-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="35b67-105">除非您明確加入宣告，否則不會收集任何資料。</span><span class="sxs-lookup"><span data-stu-id="35b67-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35b67-106">句法</span><span class="sxs-lookup"><span data-stu-id="35b67-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35b67-107">說明</span><span class="sxs-lookup"><span data-stu-id="35b67-107">DESCRIPTION</span></span>
<span data-ttu-id="35b67-108">您可以透過加入宣告資料收集來改善使用 Microsoft 雲端和 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="35b67-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="35b67-109">Azure PowerShell 不會在未經您同意的情況下收集資料，您必須在第一次執行 Cmdlet 時，在 Azure PowerShell 提示您 AzureRmDataCollection 收集資料時，再回答 [是]。</span><span class="sxs-lookup"><span data-stu-id="35b67-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="35b67-110">Microsoft 匯總收集的資料，以識別使用方式、找出常見問題，以及改善使用 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="35b67-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="35b67-111">Microsoft Azure PowerShell 不會收集任何私人資料，或任何個人的可識別資訊。</span><span class="sxs-lookup"><span data-stu-id="35b67-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="35b67-112">執行 Enable-AzureRMDataCollection Cmdlet，在目前的電腦上啟用目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="35b67-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="35b67-113">這可防止目前的使用者在第一次執行 Cmdlet 時收到關於資料收集的提示。</span><span class="sxs-lookup"><span data-stu-id="35b67-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="35b67-114">若要停用目前使用者的資料收集，請執行 Disable-AzureRmDataCollection Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35b67-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="35b67-115">示例</span><span class="sxs-lookup"><span data-stu-id="35b67-115">EXAMPLES</span></span>

### <span data-ttu-id="35b67-116">範例1：為目前的使用者啟用資料收集</span><span class="sxs-lookup"><span data-stu-id="35b67-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="35b67-117">此範例說明如何為目前的使用者啟用資料收集。</span><span class="sxs-lookup"><span data-stu-id="35b67-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="35b67-118">參數</span><span class="sxs-lookup"><span data-stu-id="35b67-118">PARAMETERS</span></span>

### <span data-ttu-id="35b67-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b67-119">-DefaultProfile</span></span>
<span data-ttu-id="35b67-120">用於與 azure 進行通訊的認證、帳戶、租使用者與訂閱。</span><span class="sxs-lookup"><span data-stu-id="35b67-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b67-121">-確認</span><span class="sxs-lookup"><span data-stu-id="35b67-121">-Confirm</span></span>
<span data-ttu-id="35b67-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="35b67-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35b67-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35b67-123">-WhatIf</span></span>
<span data-ttu-id="35b67-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="35b67-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35b67-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35b67-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35b67-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b67-126">CommonParameters</span></span>
<span data-ttu-id="35b67-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35b67-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b67-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="35b67-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b67-129">輸入</span><span class="sxs-lookup"><span data-stu-id="35b67-129">INPUTS</span></span>

### <span data-ttu-id="35b67-130">所有</span><span class="sxs-lookup"><span data-stu-id="35b67-130">None</span></span>

## <span data-ttu-id="35b67-131">輸出</span><span class="sxs-lookup"><span data-stu-id="35b67-131">OUTPUTS</span></span>

### <span data-ttu-id="35b67-132">System.void</span><span class="sxs-lookup"><span data-stu-id="35b67-132">System.Void</span></span>

## <span data-ttu-id="35b67-133">筆記</span><span class="sxs-lookup"><span data-stu-id="35b67-133">NOTES</span></span>

## <span data-ttu-id="35b67-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="35b67-134">RELATED LINKS</span></span>

[<span data-ttu-id="35b67-135">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="35b67-135">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)
