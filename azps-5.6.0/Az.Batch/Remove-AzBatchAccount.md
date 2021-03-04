---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: 5b74f378bc867c1d39f27ebdd9972dfdda5457c2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916286"
---
# <span data-ttu-id="fd5b9-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="fd5b9-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="fd5b9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="fd5b9-103">移除批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-103">Removes a Batch account.</span></span>

## <span data-ttu-id="fd5b9-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd5b9-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd5b9-105">描述</span><span class="sxs-lookup"><span data-stu-id="fd5b9-105">DESCRIPTION</span></span>
<span data-ttu-id="fd5b9-106">**Remove-AzBatchAccount** Cmdlet 會移除 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="fd5b9-107">除非您指定 *Force* 參數，否則此 Cmdlet 會先提示您，然後再移除帳戶。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="fd5b9-108">例子</span><span class="sxs-lookup"><span data-stu-id="fd5b9-108">EXAMPLES</span></span>

### <span data-ttu-id="fd5b9-109">範例 1：移除批次帳戶</span><span class="sxs-lookup"><span data-stu-id="fd5b9-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="fd5b9-110">此命令會移除名為 pfuller 的 Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="fd5b9-111">此命令會先提示您確認，然後再刪除帳戶。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="fd5b9-112">參數</span><span class="sxs-lookup"><span data-stu-id="fd5b9-112">PARAMETERS</span></span>

### <span data-ttu-id="fd5b9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fd5b9-113">-AccountName</span></span>
<span data-ttu-id="fd5b9-114">指定此 Cmdlet 移除的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd5b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd5b9-115">-DefaultProfile</span></span>
<span data-ttu-id="fd5b9-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd5b9-117">-強制</span><span class="sxs-lookup"><span data-stu-id="fd5b9-117">-Force</span></span>
<span data-ttu-id="fd5b9-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd5b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd5b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd5b9-120">指定此 Cmdlet 移除之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd5b9-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fd5b9-121">-Confirm</span></span>
<span data-ttu-id="fd5b9-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd5b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd5b9-123">-WhatIf</span></span>
<span data-ttu-id="fd5b9-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd5b9-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd5b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd5b9-126">CommonParameters</span></span>
<span data-ttu-id="fd5b9-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd5b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd5b9-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd5b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd5b9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fd5b9-129">INPUTS</span></span>

### <span data-ttu-id="fd5b9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fd5b9-130">System.String</span></span>

## <span data-ttu-id="fd5b9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fd5b9-131">OUTPUTS</span></span>

### <span data-ttu-id="fd5b9-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="fd5b9-132">System.Void</span></span>

## <span data-ttu-id="fd5b9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fd5b9-133">NOTES</span></span>

## <span data-ttu-id="fd5b9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd5b9-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd5b9-135">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="fd5b9-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="fd5b9-136">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="fd5b9-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="fd5b9-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="fd5b9-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="fd5b9-138">Azure Batch Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fd5b9-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
