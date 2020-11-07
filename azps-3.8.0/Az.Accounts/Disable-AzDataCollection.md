---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2020
ms.locfileid: "93966526"
---
# <span data-ttu-id="f4c53-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f4c53-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="f4c53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4c53-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c53-103">在收集資料時，無法改善 Azure PowerShell Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4c53-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="f4c53-104">預設會收集資料，除非您明確退出宣告。</span><span class="sxs-lookup"><span data-stu-id="f4c53-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="f4c53-105">句法</span><span class="sxs-lookup"><span data-stu-id="f4c53-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c53-106">說明</span><span class="sxs-lookup"><span data-stu-id="f4c53-106">DESCRIPTION</span></span>

<span data-ttu-id="f4c53-107">這個 `Disable-AzDataCollection` Cmdlet 是用來退出宣告資料收集。</span><span class="sxs-lookup"><span data-stu-id="f4c53-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="f4c53-108">Azure PowerShell 預設會自動收集遙測資料。</span><span class="sxs-lookup"><span data-stu-id="f4c53-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="f4c53-109">若要停用資料收集，您必須明確退出宣告。Microsoft 會匯總收集的資料以識別使用方式、找出常見問題，以及改善 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="f4c53-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="f4c53-110">Microsoft Azure PowerShell 不會收集任何私人或個人資料。</span><span class="sxs-lookup"><span data-stu-id="f4c53-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="f4c53-111">如果您先前已退出宣告，請執行 `Enable-AzDataCollection` Cmdlet，在目前的電腦上重新啟用目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="f4c53-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="f4c53-112">示例</span><span class="sxs-lookup"><span data-stu-id="f4c53-112">EXAMPLES</span></span>

### <span data-ttu-id="f4c53-113">範例1：停用目前使用者的資料收集</span><span class="sxs-lookup"><span data-stu-id="f4c53-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="f4c53-114">下列範例顯示如何停用目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="f4c53-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="f4c53-115">參數</span><span class="sxs-lookup"><span data-stu-id="f4c53-115">PARAMETERS</span></span>

### <span data-ttu-id="f4c53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c53-116">-DefaultProfile</span></span>

<span data-ttu-id="f4c53-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4c53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4c53-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f4c53-118">-Confirm</span></span>

<span data-ttu-id="f4c53-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4c53-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c53-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c53-120">-WhatIf</span></span>

<span data-ttu-id="f4c53-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4c53-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4c53-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4c53-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c53-123">CommonParameters</span></span>

<span data-ttu-id="f4c53-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4c53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c53-125">如需詳細資訊，請參閱 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)。</span><span class="sxs-lookup"><span data-stu-id="f4c53-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="f4c53-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f4c53-126">INPUTS</span></span>

### <span data-ttu-id="f4c53-127">所有</span><span class="sxs-lookup"><span data-stu-id="f4c53-127">None</span></span>

## <span data-ttu-id="f4c53-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f4c53-128">OUTPUTS</span></span>

### <span data-ttu-id="f4c53-129">System.void</span><span class="sxs-lookup"><span data-stu-id="f4c53-129">System.Void</span></span>

## <span data-ttu-id="f4c53-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f4c53-130">NOTES</span></span>

## <span data-ttu-id="f4c53-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4c53-131">RELATED LINKS</span></span>

[<span data-ttu-id="f4c53-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f4c53-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
