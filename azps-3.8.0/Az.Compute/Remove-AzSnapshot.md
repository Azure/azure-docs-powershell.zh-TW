---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 686f7dbe4bba17017e1920dd2c67a05c2ccd5eae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958133"
---
# <span data-ttu-id="759f6-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="759f6-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="759f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="759f6-102">SYNOPSIS</span></span>
<span data-ttu-id="759f6-103">移除快照。</span><span class="sxs-lookup"><span data-stu-id="759f6-103">Removes a snapshot.</span></span>

## <span data-ttu-id="759f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="759f6-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="759f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="759f6-105">DESCRIPTION</span></span>
<span data-ttu-id="759f6-106">**AzSnapshot** Cmdlet 會移除快照。</span><span class="sxs-lookup"><span data-stu-id="759f6-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="759f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="759f6-107">EXAMPLES</span></span>

### <span data-ttu-id="759f6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="759f6-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="759f6-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為「Snapshot01」的快照。</span><span class="sxs-lookup"><span data-stu-id="759f6-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="759f6-110">參數</span><span class="sxs-lookup"><span data-stu-id="759f6-110">PARAMETERS</span></span>

### <span data-ttu-id="759f6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="759f6-111">-AsJob</span></span>
<span data-ttu-id="759f6-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="759f6-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="759f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759f6-113">-DefaultProfile</span></span>
<span data-ttu-id="759f6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="759f6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="759f6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="759f6-115">-Force</span></span>
<span data-ttu-id="759f6-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="759f6-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="759f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="759f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="759f6-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="759f6-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759f6-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="759f6-119">-SnapshotName</span></span>
<span data-ttu-id="759f6-120">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="759f6-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="759f6-121">-確認</span><span class="sxs-lookup"><span data-stu-id="759f6-121">-Confirm</span></span>
<span data-ttu-id="759f6-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="759f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="759f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="759f6-123">-WhatIf</span></span>
<span data-ttu-id="759f6-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="759f6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="759f6-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="759f6-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="759f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759f6-126">CommonParameters</span></span>
<span data-ttu-id="759f6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="759f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759f6-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="759f6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759f6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="759f6-129">INPUTS</span></span>

### <span data-ttu-id="759f6-130">System.object</span><span class="sxs-lookup"><span data-stu-id="759f6-130">System.String</span></span>

## <span data-ttu-id="759f6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="759f6-131">OUTPUTS</span></span>

### <span data-ttu-id="759f6-132">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="759f6-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="759f6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="759f6-133">NOTES</span></span>

## <span data-ttu-id="759f6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="759f6-134">RELATED LINKS</span></span>
