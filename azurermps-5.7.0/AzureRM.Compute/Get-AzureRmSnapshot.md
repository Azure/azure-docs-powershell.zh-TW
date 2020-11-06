---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449944"
---
# <span data-ttu-id="e1eaf-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="e1eaf-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="e1eaf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="e1eaf-103">取得快照的屬性</span><span class="sxs-lookup"><span data-stu-id="e1eaf-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1eaf-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1eaf-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e1eaf-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="e1eaf-106">**AzureRmSnapshot** Cmdlet 會取得快照的屬性。</span><span class="sxs-lookup"><span data-stu-id="e1eaf-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="e1eaf-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1eaf-107">EXAMPLES</span></span>

### <span data-ttu-id="e1eaf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e1eaf-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="e1eaf-109">這個命令會取得訂閱所有快照的屬性。</span><span class="sxs-lookup"><span data-stu-id="e1eaf-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="e1eaf-110">範例2</span><span class="sxs-lookup"><span data-stu-id="e1eaf-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="e1eaf-111">這個命令會取得名為 "ResourceGroupName1" 的資源群組中所有快照的屬性</span><span class="sxs-lookup"><span data-stu-id="e1eaf-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="e1eaf-112">範例3</span><span class="sxs-lookup"><span data-stu-id="e1eaf-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="e1eaf-113">這個命令會取得名為 "ResourceGroupName1" 的資源群組中名為 "SnapshotName1" 的快照屬性</span><span class="sxs-lookup"><span data-stu-id="e1eaf-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="e1eaf-114">參數</span><span class="sxs-lookup"><span data-stu-id="e1eaf-114">PARAMETERS</span></span>

### <span data-ttu-id="e1eaf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1eaf-115">-ResourceGroupName</span></span>
<span data-ttu-id="e1eaf-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1eaf-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e1eaf-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e1eaf-117">-SnapshotName</span></span>
<span data-ttu-id="e1eaf-118">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1eaf-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="e1eaf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1eaf-119">CommonParameters</span></span>
<span data-ttu-id="e1eaf-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1eaf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1eaf-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1eaf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1eaf-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e1eaf-122">INPUTS</span></span>

### <span data-ttu-id="e1eaf-123">System.object</span><span class="sxs-lookup"><span data-stu-id="e1eaf-123">System.String</span></span>

## <span data-ttu-id="e1eaf-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e1eaf-124">OUTPUTS</span></span>

### <span data-ttu-id="e1eaf-125">System.object</span><span class="sxs-lookup"><span data-stu-id="e1eaf-125">System.Object</span></span>

## <span data-ttu-id="e1eaf-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e1eaf-126">NOTES</span></span>

## <span data-ttu-id="e1eaf-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1eaf-127">RELATED LINKS</span></span>

