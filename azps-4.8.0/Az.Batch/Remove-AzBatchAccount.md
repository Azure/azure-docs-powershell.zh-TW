---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchAccount.md
ms.openlocfilehash: ae67aac391f2cce2a37be8a5a15a0fd0ea37cdd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128540"
---
# <span data-ttu-id="7d637-101">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7d637-101">Remove-AzBatchAccount</span></span>

## <span data-ttu-id="7d637-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d637-102">SYNOPSIS</span></span>
<span data-ttu-id="7d637-103">移除批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="7d637-103">Removes a Batch account.</span></span>

## <span data-ttu-id="7d637-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d637-104">SYNTAX</span></span>

```
Remove-AzBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d637-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d637-105">DESCRIPTION</span></span>
<span data-ttu-id="7d637-106">**AzBatchAccount** Cmdlet 會移除 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="7d637-106">The **Remove-AzBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="7d637-107">除非您指定 *Force* 參數，否則此 Cmdlet 會在移除帳戶之前提示您。</span><span class="sxs-lookup"><span data-stu-id="7d637-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="7d637-108">示例</span><span class="sxs-lookup"><span data-stu-id="7d637-108">EXAMPLES</span></span>

### <span data-ttu-id="7d637-109">範例1：移除批次帳戶</span><span class="sxs-lookup"><span data-stu-id="7d637-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="7d637-110">這個命令會移除名為 pfuller 的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="7d637-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="7d637-111">這個命令會在您刪除帳戶之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d637-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="7d637-112">參數</span><span class="sxs-lookup"><span data-stu-id="7d637-112">PARAMETERS</span></span>

### <span data-ttu-id="7d637-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7d637-113">-AccountName</span></span>
<span data-ttu-id="7d637-114">指定此 Cmdlet 移除的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7d637-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d637-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d637-115">-DefaultProfile</span></span>
<span data-ttu-id="7d637-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d637-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d637-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7d637-117">-Force</span></span>
<span data-ttu-id="7d637-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7d637-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d637-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d637-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d637-120">指定此 Cmdlet 移除之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7d637-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d637-121">-確認</span><span class="sxs-lookup"><span data-stu-id="7d637-121">-Confirm</span></span>
<span data-ttu-id="7d637-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d637-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d637-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d637-123">-WhatIf</span></span>
<span data-ttu-id="7d637-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d637-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d637-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d637-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d637-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d637-126">CommonParameters</span></span>
<span data-ttu-id="7d637-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d637-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d637-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7d637-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d637-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7d637-129">INPUTS</span></span>

### <span data-ttu-id="7d637-130">System.object</span><span class="sxs-lookup"><span data-stu-id="7d637-130">System.String</span></span>

## <span data-ttu-id="7d637-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7d637-131">OUTPUTS</span></span>

### <span data-ttu-id="7d637-132">System.void</span><span class="sxs-lookup"><span data-stu-id="7d637-132">System.Void</span></span>

## <span data-ttu-id="7d637-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7d637-133">NOTES</span></span>

## <span data-ttu-id="7d637-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d637-134">RELATED LINKS</span></span>

[<span data-ttu-id="7d637-135">AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7d637-135">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="7d637-136">新-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7d637-136">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="7d637-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7d637-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="7d637-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7d637-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
