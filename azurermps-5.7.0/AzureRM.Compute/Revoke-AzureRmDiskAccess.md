---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 2b9573e3add842478977cf620873d3cf0cfdaa8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455488"
---
# <span data-ttu-id="53462-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="53462-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="53462-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53462-102">SYNOPSIS</span></span>
<span data-ttu-id="53462-103">吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="53462-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53462-104">句法</span><span class="sxs-lookup"><span data-stu-id="53462-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53462-105">說明</span><span class="sxs-lookup"><span data-stu-id="53462-105">DESCRIPTION</span></span>
<span data-ttu-id="53462-106">**Revoke AzureRmDiskAccess** Cmdlet 會吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="53462-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="53462-107">示例</span><span class="sxs-lookup"><span data-stu-id="53462-107">EXAMPLES</span></span>

### <span data-ttu-id="53462-108">範例1</span><span class="sxs-lookup"><span data-stu-id="53462-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="53462-109">在名為 "ResourceGroup01" 的資源群組中，廢除名為「Disk01」的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="53462-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="53462-110">參數</span><span class="sxs-lookup"><span data-stu-id="53462-110">PARAMETERS</span></span>

### <span data-ttu-id="53462-111">-DiskName</span><span class="sxs-lookup"><span data-stu-id="53462-111">-DiskName</span></span>
<span data-ttu-id="53462-112">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="53462-112">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="53462-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53462-113">-ResourceGroupName</span></span>
<span data-ttu-id="53462-114">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="53462-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="53462-115">-確認</span><span class="sxs-lookup"><span data-stu-id="53462-115">-Confirm</span></span>
<span data-ttu-id="53462-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53462-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53462-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53462-117">-WhatIf</span></span>
<span data-ttu-id="53462-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53462-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53462-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53462-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53462-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53462-120">CommonParameters</span></span>
<span data-ttu-id="53462-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53462-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53462-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53462-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53462-123">輸入</span><span class="sxs-lookup"><span data-stu-id="53462-123">INPUTS</span></span>

### <span data-ttu-id="53462-124">System.object</span><span class="sxs-lookup"><span data-stu-id="53462-124">System.String</span></span>

## <span data-ttu-id="53462-125">輸出</span><span class="sxs-lookup"><span data-stu-id="53462-125">OUTPUTS</span></span>

### <span data-ttu-id="53462-126">System.object</span><span class="sxs-lookup"><span data-stu-id="53462-126">System.Object</span></span>

## <span data-ttu-id="53462-127">筆記</span><span class="sxs-lookup"><span data-stu-id="53462-127">NOTES</span></span>

## <span data-ttu-id="53462-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="53462-128">RELATED LINKS</span></span>

