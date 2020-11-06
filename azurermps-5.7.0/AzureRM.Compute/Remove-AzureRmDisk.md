---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmDisk.md
ms.openlocfilehash: 10150d7941aa3b17a0a7d4447ff0a57e3d04a516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446355"
---
# <span data-ttu-id="2be63-101">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2be63-101">Remove-AzureRmDisk</span></span>

## <span data-ttu-id="2be63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2be63-102">SYNOPSIS</span></span>
<span data-ttu-id="2be63-103">移除磁片。</span><span class="sxs-lookup"><span data-stu-id="2be63-103">Removes a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2be63-104">句法</span><span class="sxs-lookup"><span data-stu-id="2be63-104">SYNTAX</span></span>

```
Remove-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2be63-105">說明</span><span class="sxs-lookup"><span data-stu-id="2be63-105">DESCRIPTION</span></span>
<span data-ttu-id="2be63-106">**AzureRmDisk** Cmdlet 會移除磁片。</span><span class="sxs-lookup"><span data-stu-id="2be63-106">The **Remove-AzureRmDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="2be63-107">示例</span><span class="sxs-lookup"><span data-stu-id="2be63-107">EXAMPLES</span></span>

### <span data-ttu-id="2be63-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2be63-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="2be63-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為「Disk01」的磁片。</span><span class="sxs-lookup"><span data-stu-id="2be63-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2be63-110">參數</span><span class="sxs-lookup"><span data-stu-id="2be63-110">PARAMETERS</span></span>

### <span data-ttu-id="2be63-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="2be63-111">-DiskName</span></span>
<span data-ttu-id="2be63-112">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="2be63-112">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2be63-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2be63-113">-Force</span></span>
<span data-ttu-id="2be63-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2be63-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be63-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be63-115">-ResourceGroupName</span></span>
<span data-ttu-id="2be63-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2be63-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2be63-117">-確認</span><span class="sxs-lookup"><span data-stu-id="2be63-117">-Confirm</span></span>
<span data-ttu-id="2be63-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2be63-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be63-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be63-119">-WhatIf</span></span>
<span data-ttu-id="2be63-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2be63-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be63-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2be63-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be63-122">CommonParameters</span></span>
<span data-ttu-id="2be63-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2be63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be63-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2be63-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be63-125">輸入</span><span class="sxs-lookup"><span data-stu-id="2be63-125">INPUTS</span></span>

### <span data-ttu-id="2be63-126">System.object</span><span class="sxs-lookup"><span data-stu-id="2be63-126">System.String</span></span>

## <span data-ttu-id="2be63-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2be63-127">OUTPUTS</span></span>

### <span data-ttu-id="2be63-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2be63-128">System.Object</span></span>

## <span data-ttu-id="2be63-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2be63-129">NOTES</span></span>

## <span data-ttu-id="2be63-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2be63-130">RELATED LINKS</span></span>

