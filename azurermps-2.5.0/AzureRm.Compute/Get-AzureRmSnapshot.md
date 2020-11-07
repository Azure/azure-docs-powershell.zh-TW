---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 8133bfc8381f08e69afbd6bfbd3a25084e9eb2b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800562"
---
# <span data-ttu-id="c1739-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c1739-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="c1739-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1739-102">SYNOPSIS</span></span>
<span data-ttu-id="c1739-103">取得快照的屬性</span><span class="sxs-lookup"><span data-stu-id="c1739-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1739-104">句法</span><span class="sxs-lookup"><span data-stu-id="c1739-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1739-105">說明</span><span class="sxs-lookup"><span data-stu-id="c1739-105">DESCRIPTION</span></span>
<span data-ttu-id="c1739-106">**AzureRmSnapshot** Cmdlet 會取得快照的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1739-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="c1739-107">示例</span><span class="sxs-lookup"><span data-stu-id="c1739-107">EXAMPLES</span></span>

### <span data-ttu-id="c1739-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c1739-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="c1739-109">這個命令會取得訂閱所有快照的屬性。</span><span class="sxs-lookup"><span data-stu-id="c1739-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="c1739-110">範例2</span><span class="sxs-lookup"><span data-stu-id="c1739-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="c1739-111">這個命令會取得名為 "ResourceGroupName1" 的資源群組中所有快照的屬性</span><span class="sxs-lookup"><span data-stu-id="c1739-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="c1739-112">範例3</span><span class="sxs-lookup"><span data-stu-id="c1739-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="c1739-113">這個命令會取得名為 "ResourceGroupName1" 的資源群組中名為 "SnapshotName1" 的快照屬性</span><span class="sxs-lookup"><span data-stu-id="c1739-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="c1739-114">參數</span><span class="sxs-lookup"><span data-stu-id="c1739-114">PARAMETERS</span></span>

### <span data-ttu-id="c1739-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1739-115">-DefaultProfile</span></span>
<span data-ttu-id="c1739-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1739-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1739-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1739-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1739-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1739-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c1739-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="c1739-119">-SnapshotName</span></span>
<span data-ttu-id="c1739-120">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="c1739-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="c1739-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1739-121">CommonParameters</span></span>
<span data-ttu-id="c1739-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1739-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1739-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1739-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1739-124">輸入</span><span class="sxs-lookup"><span data-stu-id="c1739-124">INPUTS</span></span>

### <span data-ttu-id="c1739-125">System.object</span><span class="sxs-lookup"><span data-stu-id="c1739-125">System.String</span></span>

## <span data-ttu-id="c1739-126">輸出</span><span class="sxs-lookup"><span data-stu-id="c1739-126">OUTPUTS</span></span>

### <span data-ttu-id="c1739-127">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="c1739-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="c1739-128">筆記</span><span class="sxs-lookup"><span data-stu-id="c1739-128">NOTES</span></span>

## <span data-ttu-id="c1739-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1739-129">RELATED LINKS</span></span>

