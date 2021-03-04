---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzSnapshot.md
ms.openlocfilehash: 86eb9f1389f0474fcc109b219e9eae1bd385b7b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912045"
---
# <span data-ttu-id="0ce21-101">Remove-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="0ce21-101">Remove-AzSnapshot</span></span>

## <span data-ttu-id="0ce21-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0ce21-102">SYNOPSIS</span></span>
<span data-ttu-id="0ce21-103">移除快照。</span><span class="sxs-lookup"><span data-stu-id="0ce21-103">Removes a snapshot.</span></span>

## <span data-ttu-id="0ce21-104">語法</span><span class="sxs-lookup"><span data-stu-id="0ce21-104">SYNTAX</span></span>

```
Remove-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ce21-105">描述</span><span class="sxs-lookup"><span data-stu-id="0ce21-105">DESCRIPTION</span></span>
<span data-ttu-id="0ce21-106">**Remove-AzSnapshot** Cmdlet 會移除快照。</span><span class="sxs-lookup"><span data-stu-id="0ce21-106">The **Remove-AzSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="0ce21-107">例子</span><span class="sxs-lookup"><span data-stu-id="0ce21-107">EXAMPLES</span></span>

### <span data-ttu-id="0ce21-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0ce21-108">Example 1</span></span>
```
PS C:\> Remove-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="0ce21-109">此命令會移除資源群組 "ResourceGroup01" 中名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="0ce21-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0ce21-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ce21-110">PARAMETERS</span></span>

### <span data-ttu-id="0ce21-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ce21-111">-AsJob</span></span>
<span data-ttu-id="0ce21-112">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="0ce21-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0ce21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ce21-113">-DefaultProfile</span></span>
<span data-ttu-id="0ce21-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0ce21-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ce21-115">-強制</span><span class="sxs-lookup"><span data-stu-id="0ce21-115">-Force</span></span>
<span data-ttu-id="0ce21-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="0ce21-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0ce21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ce21-117">-ResourceGroupName</span></span>
<span data-ttu-id="0ce21-118">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0ce21-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0ce21-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="0ce21-119">-SnapshotName</span></span>
<span data-ttu-id="0ce21-120">指定快照名稱。</span><span class="sxs-lookup"><span data-stu-id="0ce21-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="0ce21-121">-確認</span><span class="sxs-lookup"><span data-stu-id="0ce21-121">-Confirm</span></span>
<span data-ttu-id="0ce21-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0ce21-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ce21-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ce21-123">-WhatIf</span></span>
<span data-ttu-id="0ce21-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0ce21-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ce21-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0ce21-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ce21-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ce21-126">CommonParameters</span></span>
<span data-ttu-id="0ce21-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0ce21-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ce21-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ce21-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ce21-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0ce21-129">INPUTS</span></span>

### <span data-ttu-id="0ce21-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0ce21-130">System.String</span></span>

## <span data-ttu-id="0ce21-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0ce21-131">OUTPUTS</span></span>

### <span data-ttu-id="0ce21-132">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0ce21-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0ce21-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0ce21-133">NOTES</span></span>

## <span data-ttu-id="0ce21-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0ce21-134">RELATED LINKS</span></span>
