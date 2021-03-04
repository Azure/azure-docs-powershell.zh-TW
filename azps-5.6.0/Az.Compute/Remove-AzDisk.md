---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: c53d49397c79f12500b2a7bbccbec2781f27b610
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905181"
---
# <span data-ttu-id="7c793-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="7c793-101">Remove-AzDisk</span></span>

## <span data-ttu-id="7c793-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7c793-102">SYNOPSIS</span></span>
<span data-ttu-id="7c793-103">移除磁片。</span><span class="sxs-lookup"><span data-stu-id="7c793-103">Removes a disk.</span></span>

## <span data-ttu-id="7c793-104">語法</span><span class="sxs-lookup"><span data-stu-id="7c793-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c793-105">描述</span><span class="sxs-lookup"><span data-stu-id="7c793-105">DESCRIPTION</span></span>
<span data-ttu-id="7c793-106">**Remove-Az移除** Cmdlet 會移除磁片。</span><span class="sxs-lookup"><span data-stu-id="7c793-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="7c793-107">例子</span><span class="sxs-lookup"><span data-stu-id="7c793-107">EXAMPLES</span></span>

### <span data-ttu-id="7c793-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7c793-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="7c793-109">此命令會移除資源群組 "ResourceGroup01" 中名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="7c793-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7c793-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c793-110">PARAMETERS</span></span>

### <span data-ttu-id="7c793-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c793-111">-AsJob</span></span>
<span data-ttu-id="7c793-112">在背景中執行 Cmdlet 並返回工作以追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="7c793-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7c793-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c793-113">-DefaultProfile</span></span>
<span data-ttu-id="7c793-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c793-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c793-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="7c793-115">-DiskName</span></span>
<span data-ttu-id="7c793-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c793-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="7c793-117">-強制</span><span class="sxs-lookup"><span data-stu-id="7c793-117">-Force</span></span>
<span data-ttu-id="7c793-118">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7c793-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c793-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c793-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c793-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c793-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7c793-121">-確認</span><span class="sxs-lookup"><span data-stu-id="7c793-121">-Confirm</span></span>
<span data-ttu-id="7c793-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7c793-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c793-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c793-123">-WhatIf</span></span>
<span data-ttu-id="7c793-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c793-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c793-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c793-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c793-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c793-126">CommonParameters</span></span>
<span data-ttu-id="7c793-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7c793-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c793-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c793-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c793-129">輸入</span><span class="sxs-lookup"><span data-stu-id="7c793-129">INPUTS</span></span>

### <span data-ttu-id="7c793-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7c793-130">System.String</span></span>

## <span data-ttu-id="7c793-131">輸出</span><span class="sxs-lookup"><span data-stu-id="7c793-131">OUTPUTS</span></span>

### <span data-ttu-id="7c793-132">Microsoft.Azure.Commands.Compute.Automation.models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7c793-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7c793-133">筆記</span><span class="sxs-lookup"><span data-stu-id="7c793-133">NOTES</span></span>

## <span data-ttu-id="7c793-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c793-134">RELATED LINKS</span></span>
