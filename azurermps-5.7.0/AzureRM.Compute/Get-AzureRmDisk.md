---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449948"
---
# <span data-ttu-id="abb2a-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="abb2a-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="abb2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="abb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="abb2a-103">取得磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="abb2a-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="abb2a-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="abb2a-105">說明</span><span class="sxs-lookup"><span data-stu-id="abb2a-105">DESCRIPTION</span></span>
<span data-ttu-id="abb2a-106">**AzureRmDisk** Cmdlet 會取得磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="abb2a-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="abb2a-107">示例</span><span class="sxs-lookup"><span data-stu-id="abb2a-107">EXAMPLES</span></span>

### <span data-ttu-id="abb2a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="abb2a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="abb2a-109">這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Disk01 ' 磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="abb2a-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="abb2a-110">範例2</span><span class="sxs-lookup"><span data-stu-id="abb2a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="abb2a-111">這個命令會取得資源群組 ' ResourceGroup01 ' 中所有磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="abb2a-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="abb2a-112">範例3</span><span class="sxs-lookup"><span data-stu-id="abb2a-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="abb2a-113">這個命令會取得訂閱下所有磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="abb2a-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="abb2a-114">參數</span><span class="sxs-lookup"><span data-stu-id="abb2a-114">PARAMETERS</span></span>

### <span data-ttu-id="abb2a-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="abb2a-115">-DiskName</span></span>
<span data-ttu-id="abb2a-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="abb2a-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abb2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="abb2a-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="abb2a-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb2a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb2a-119">CommonParameters</span></span>
<span data-ttu-id="abb2a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="abb2a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb2a-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="abb2a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb2a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="abb2a-122">INPUTS</span></span>

### <span data-ttu-id="abb2a-123">System.object</span><span class="sxs-lookup"><span data-stu-id="abb2a-123">System.String</span></span>

## <span data-ttu-id="abb2a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="abb2a-124">OUTPUTS</span></span>

### <span data-ttu-id="abb2a-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="abb2a-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="abb2a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="abb2a-126">NOTES</span></span>

## <span data-ttu-id="abb2a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="abb2a-127">RELATED LINKS</span></span>

