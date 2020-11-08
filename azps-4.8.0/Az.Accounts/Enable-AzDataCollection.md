---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127866"
---
# <span data-ttu-id="31e2b-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="31e2b-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="31e2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="31e2b-103">啟用 Azure PowerShell 以收集資料，以使用 Azure PowerShell Cmdlet 來改善使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="31e2b-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="31e2b-104">執行此 Cmdlet 會將您的目前使用者的資料收集加入到目前的電腦上。</span><span class="sxs-lookup"><span data-stu-id="31e2b-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="31e2b-105">預設會收集資料，除非您明確退出宣告。</span><span class="sxs-lookup"><span data-stu-id="31e2b-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="31e2b-106">句法</span><span class="sxs-lookup"><span data-stu-id="31e2b-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31e2b-107">說明</span><span class="sxs-lookup"><span data-stu-id="31e2b-107">DESCRIPTION</span></span>

<span data-ttu-id="31e2b-108">這個 `Enable-AzDataCollection` Cmdlet 是用來加入宣告資料收集。</span><span class="sxs-lookup"><span data-stu-id="31e2b-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="31e2b-109">Azure PowerShell 預設會自動收集遙測資料。</span><span class="sxs-lookup"><span data-stu-id="31e2b-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="31e2b-110">Microsoft 會匯總收集的資料以識別使用方式、找出常見問題，以及改善 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="31e2b-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="31e2b-111">Microsoft Azure PowerShell 不會收集任何私人或個人資料。</span><span class="sxs-lookup"><span data-stu-id="31e2b-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="31e2b-112">若要停用資料收集，您必須透過執行明確退出宣告 `Disable-AzDataCollection` 。</span><span class="sxs-lookup"><span data-stu-id="31e2b-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="31e2b-113">示例</span><span class="sxs-lookup"><span data-stu-id="31e2b-113">EXAMPLES</span></span>

### <span data-ttu-id="31e2b-114">範例1：為目前的使用者啟用資料收集</span><span class="sxs-lookup"><span data-stu-id="31e2b-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="31e2b-115">下列範例顯示如何為目前的使用者啟用資料收集。</span><span class="sxs-lookup"><span data-stu-id="31e2b-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="31e2b-116">參數</span><span class="sxs-lookup"><span data-stu-id="31e2b-116">PARAMETERS</span></span>

### <span data-ttu-id="31e2b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e2b-117">-DefaultProfile</span></span>

<span data-ttu-id="31e2b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31e2b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31e2b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="31e2b-119">-Confirm</span></span>

<span data-ttu-id="31e2b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="31e2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e2b-121">-WhatIf</span></span>

<span data-ttu-id="31e2b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31e2b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31e2b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31e2b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e2b-124">CommonParameters</span></span>

<span data-ttu-id="31e2b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31e2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e2b-126">如需詳細資訊，請參閱 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)。</span><span class="sxs-lookup"><span data-stu-id="31e2b-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="31e2b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="31e2b-127">INPUTS</span></span>

### <span data-ttu-id="31e2b-128">所有</span><span class="sxs-lookup"><span data-stu-id="31e2b-128">None</span></span>

## <span data-ttu-id="31e2b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="31e2b-129">OUTPUTS</span></span>

### <span data-ttu-id="31e2b-130">System.void</span><span class="sxs-lookup"><span data-stu-id="31e2b-130">System.Void</span></span>

## <span data-ttu-id="31e2b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="31e2b-131">NOTES</span></span>

## <span data-ttu-id="31e2b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="31e2b-132">RELATED LINKS</span></span>

[<span data-ttu-id="31e2b-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="31e2b-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
