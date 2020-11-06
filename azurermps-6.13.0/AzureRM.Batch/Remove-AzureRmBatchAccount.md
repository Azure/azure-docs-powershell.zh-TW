---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 89F604DD-EE77-440D-BCC9-3F74D994C447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchAccount.md
ms.openlocfilehash: 3528d66c635de78347647f0d1e451dc0b173a641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445716"
---
# <span data-ttu-id="33d85-101">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="33d85-101">Remove-AzureRmBatchAccount</span></span>

## <span data-ttu-id="33d85-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33d85-102">SYNOPSIS</span></span>
<span data-ttu-id="33d85-103">移除批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="33d85-103">Removes a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d85-104">句法</span><span class="sxs-lookup"><span data-stu-id="33d85-104">SYNTAX</span></span>

```
Remove-AzureRmBatchAccount [-AccountName] <String> [[-ResourceGroupName] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d85-105">說明</span><span class="sxs-lookup"><span data-stu-id="33d85-105">DESCRIPTION</span></span>
<span data-ttu-id="33d85-106">**AzureRmBatchAccount** Cmdlet 會移除 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="33d85-106">The **Remove-AzureRmBatchAccount** cmdlet removes an Azure Batch account.</span></span>
<span data-ttu-id="33d85-107">除非您指定 *Force* 參數，否則此 Cmdlet 會在移除帳戶之前提示您。</span><span class="sxs-lookup"><span data-stu-id="33d85-107">This cmdlet prompts you before it removes an account, unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="33d85-108">示例</span><span class="sxs-lookup"><span data-stu-id="33d85-108">EXAMPLES</span></span>

### <span data-ttu-id="33d85-109">範例1：移除批次帳戶</span><span class="sxs-lookup"><span data-stu-id="33d85-109">Example 1: Remove a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchAccount -AccountName "pfuller"
```

<span data-ttu-id="33d85-110">這個命令會移除名為 pfuller 的批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="33d85-110">This command removes the Batch account named pfuller.</span></span>
<span data-ttu-id="33d85-111">這個命令會在您刪除帳戶之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="33d85-111">This command prompts you for confirmation before it deletes the account.</span></span>

## <span data-ttu-id="33d85-112">參數</span><span class="sxs-lookup"><span data-stu-id="33d85-112">PARAMETERS</span></span>

### <span data-ttu-id="33d85-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="33d85-113">-AccountName</span></span>
<span data-ttu-id="33d85-114">指定此 Cmdlet 移除的批次帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="33d85-114">Specifies the name of the Batch account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="33d85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d85-115">-DefaultProfile</span></span>
<span data-ttu-id="33d85-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33d85-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33d85-117">-Force</span><span class="sxs-lookup"><span data-stu-id="33d85-117">-Force</span></span>
<span data-ttu-id="33d85-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="33d85-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="33d85-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d85-119">-ResourceGroupName</span></span>
<span data-ttu-id="33d85-120">指定此 Cmdlet 移除之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="33d85-120">Specifies the resource group of the account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="33d85-121">-確認</span><span class="sxs-lookup"><span data-stu-id="33d85-121">-Confirm</span></span>
<span data-ttu-id="33d85-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="33d85-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d85-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d85-123">-WhatIf</span></span>
<span data-ttu-id="33d85-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33d85-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33d85-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33d85-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d85-126">CommonParameters</span></span>
<span data-ttu-id="33d85-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33d85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d85-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33d85-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d85-129">輸入</span><span class="sxs-lookup"><span data-stu-id="33d85-129">INPUTS</span></span>

### <span data-ttu-id="33d85-130">System.object</span><span class="sxs-lookup"><span data-stu-id="33d85-130">System.String</span></span>

## <span data-ttu-id="33d85-131">輸出</span><span class="sxs-lookup"><span data-stu-id="33d85-131">OUTPUTS</span></span>

### <span data-ttu-id="33d85-132">System.void</span><span class="sxs-lookup"><span data-stu-id="33d85-132">System.Void</span></span>

## <span data-ttu-id="33d85-133">筆記</span><span class="sxs-lookup"><span data-stu-id="33d85-133">NOTES</span></span>

## <span data-ttu-id="33d85-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="33d85-134">RELATED LINKS</span></span>

[<span data-ttu-id="33d85-135">AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="33d85-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="33d85-136">新-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="33d85-136">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="33d85-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="33d85-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="33d85-138">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="33d85-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


