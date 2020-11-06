---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Grant-AzureRmDiskAccess.md
ms.openlocfilehash: 2787c1cf8a37fd5d143e95c55d3e98b625d4d82e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446372"
---
# <span data-ttu-id="d1aa2-101">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="d1aa2-101">Grant-AzureRmDiskAccess</span></span>

## <span data-ttu-id="d1aa2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="d1aa2-103">授權存取磁片。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-103">Grants an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1aa2-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1aa2-104">SYNTAX</span></span>

```
Grant-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [[-Access] <AccessLevel>]
 [[-DurationInSecond] <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1aa2-105">說明</span><span class="sxs-lookup"><span data-stu-id="d1aa2-105">DESCRIPTION</span></span>
<span data-ttu-id="d1aa2-106">**Grant AzureRmDiskAccess** Cmdlet 可授權存取磁片。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-106">The **Grant-AzureRmDiskAccess** cmdlet grants an access to a disk.</span></span>

## <span data-ttu-id="d1aa2-107">示例</span><span class="sxs-lookup"><span data-stu-id="d1aa2-107">EXAMPLES</span></span>

### <span data-ttu-id="d1aa2-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d1aa2-108">Example 1</span></span>
```
PS C:\> Grant-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="d1aa2-109">針對60秒的資源群組中名為 "Disk01" 的磁片，授與「Read」的存取權。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-109">Grant 'Read' access to the disk named 'Disk01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="d1aa2-110">參數</span><span class="sxs-lookup"><span data-stu-id="d1aa2-110">PARAMETERS</span></span>

### <span data-ttu-id="d1aa2-111">-Access</span><span class="sxs-lookup"><span data-stu-id="d1aa2-111">-Access</span></span>
<span data-ttu-id="d1aa2-112">指定存取層級。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-112">Specifies Access level.</span></span>

```yaml
Type: AccessLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1aa2-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="d1aa2-113">-DiskName</span></span>
<span data-ttu-id="d1aa2-114">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="d1aa2-115">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="d1aa2-115">-DurationInSecond</span></span>
<span data-ttu-id="d1aa2-116">指定存取持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-116">Specifies access duration in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1aa2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1aa2-117">-ResourceGroupName</span></span>
<span data-ttu-id="d1aa2-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d1aa2-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d1aa2-119">-Confirm</span></span>
<span data-ttu-id="d1aa2-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1aa2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1aa2-121">-WhatIf</span></span>
<span data-ttu-id="d1aa2-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d1aa2-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1aa2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1aa2-124">CommonParameters</span></span>
<span data-ttu-id="d1aa2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1aa2-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1aa2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1aa2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d1aa2-127">INPUTS</span></span>

### <span data-ttu-id="d1aa2-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d1aa2-128">System.String</span></span>

## <span data-ttu-id="d1aa2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d1aa2-129">OUTPUTS</span></span>

### <span data-ttu-id="d1aa2-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d1aa2-130">System.Object</span></span>

## <span data-ttu-id="d1aa2-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d1aa2-131">NOTES</span></span>

## <span data-ttu-id="d1aa2-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1aa2-132">RELATED LINKS</span></span>
