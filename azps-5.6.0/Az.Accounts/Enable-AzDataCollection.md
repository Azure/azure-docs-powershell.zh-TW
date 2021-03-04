---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: ce2c4060d6471cc65c6b343e86c1e15b74ca5414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914206"
---
# <span data-ttu-id="a970e-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="a970e-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="a970e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a970e-102">SYNOPSIS</span></span>
<span data-ttu-id="a970e-103">讓 Azure PowerShell 收集資料以改善 Azure PowerShell Cmdlet 的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="a970e-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a970e-104">執行此 Cmdlet 會加入宣告目前電腦上目前使用者的資料收集。</span><span class="sxs-lookup"><span data-stu-id="a970e-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="a970e-105">除非您明確退出宣告，否則預設會收集資料。</span><span class="sxs-lookup"><span data-stu-id="a970e-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="a970e-106">語法</span><span class="sxs-lookup"><span data-stu-id="a970e-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a970e-107">描述</span><span class="sxs-lookup"><span data-stu-id="a970e-107">DESCRIPTION</span></span>

<span data-ttu-id="a970e-108">`Enable-AzDataCollection`Cmdlet 是用來加入宣告資料收集。</span><span class="sxs-lookup"><span data-stu-id="a970e-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="a970e-109">Azure PowerShell 預設會自動收集遙測資料。</span><span class="sxs-lookup"><span data-stu-id="a970e-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="a970e-110">Microsoft 會匯總收集的資料，以識別使用模式、識別常見問題，以及改善 Azure PowerShell 的體驗。</span><span class="sxs-lookup"><span data-stu-id="a970e-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="a970e-111">Microsoft Azure PowerShell 不會收集任何私人或個人資料。</span><span class="sxs-lookup"><span data-stu-id="a970e-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="a970e-112">若要停用資料收集，您必須執行明確退出宣告 `Disable-AzDataCollection` 。</span><span class="sxs-lookup"><span data-stu-id="a970e-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="a970e-113">例子</span><span class="sxs-lookup"><span data-stu-id="a970e-113">EXAMPLES</span></span>

### <span data-ttu-id="a970e-114">範例 1：為目前使用者啟用資料收集</span><span class="sxs-lookup"><span data-stu-id="a970e-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="a970e-115">下列範例顯示如何為目前使用者啟用資料收集。</span><span class="sxs-lookup"><span data-stu-id="a970e-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="a970e-116">參數</span><span class="sxs-lookup"><span data-stu-id="a970e-116">PARAMETERS</span></span>

### <span data-ttu-id="a970e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a970e-117">-DefaultProfile</span></span>

<span data-ttu-id="a970e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a970e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a970e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a970e-119">-Confirm</span></span>

<span data-ttu-id="a970e-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a970e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a970e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a970e-121">-WhatIf</span></span>

<span data-ttu-id="a970e-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a970e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a970e-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a970e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a970e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a970e-124">CommonParameters</span></span>
<span data-ttu-id="a970e-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a970e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a970e-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a970e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a970e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a970e-127">INPUTS</span></span>

### <span data-ttu-id="a970e-128">沒有</span><span class="sxs-lookup"><span data-stu-id="a970e-128">None</span></span>

## <span data-ttu-id="a970e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a970e-129">OUTPUTS</span></span>

### <span data-ttu-id="a970e-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="a970e-130">System.Void</span></span>

## <span data-ttu-id="a970e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a970e-131">NOTES</span></span>

## <span data-ttu-id="a970e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a970e-132">RELATED LINKS</span></span>

[<span data-ttu-id="a970e-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="a970e-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
