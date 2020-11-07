---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796310"
---
# <span data-ttu-id="91eb7-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="91eb7-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="91eb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="91eb7-103">取得快照的屬性</span><span class="sxs-lookup"><span data-stu-id="91eb7-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="91eb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="91eb7-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91eb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="91eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="91eb7-106">**AzSnapshot** Cmdlet 會取得快照的屬性。</span><span class="sxs-lookup"><span data-stu-id="91eb7-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="91eb7-107">示例</span><span class="sxs-lookup"><span data-stu-id="91eb7-107">EXAMPLES</span></span>

### <span data-ttu-id="91eb7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="91eb7-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="91eb7-109">這個命令會取得訂閱所有快照的屬性。</span><span class="sxs-lookup"><span data-stu-id="91eb7-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="91eb7-110">範例2</span><span class="sxs-lookup"><span data-stu-id="91eb7-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="91eb7-111">這個命令會取得名為 "ResourceGroupName1" 的資源群組中所有快照的屬性</span><span class="sxs-lookup"><span data-stu-id="91eb7-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="91eb7-112">範例3</span><span class="sxs-lookup"><span data-stu-id="91eb7-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="91eb7-113">這個命令會取得名為 "ResourceGroupName1" 的資源群組中名為 "SnapshotName1" 的快照屬性</span><span class="sxs-lookup"><span data-stu-id="91eb7-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="91eb7-114">參數</span><span class="sxs-lookup"><span data-stu-id="91eb7-114">PARAMETERS</span></span>

### <span data-ttu-id="91eb7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91eb7-115">-DefaultProfile</span></span>
<span data-ttu-id="91eb7-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91eb7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91eb7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91eb7-117">-ResourceGroupName</span></span>
<span data-ttu-id="91eb7-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91eb7-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="91eb7-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="91eb7-119">-SnapshotName</span></span>
<span data-ttu-id="91eb7-120">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="91eb7-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="91eb7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91eb7-121">CommonParameters</span></span>
<span data-ttu-id="91eb7-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91eb7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91eb7-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91eb7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91eb7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="91eb7-124">INPUTS</span></span>

### <span data-ttu-id="91eb7-125">System.object</span><span class="sxs-lookup"><span data-stu-id="91eb7-125">System.String</span></span>

## <span data-ttu-id="91eb7-126">輸出</span><span class="sxs-lookup"><span data-stu-id="91eb7-126">OUTPUTS</span></span>

### <span data-ttu-id="91eb7-127">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="91eb7-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="91eb7-128">筆記</span><span class="sxs-lookup"><span data-stu-id="91eb7-128">NOTES</span></span>

## <span data-ttu-id="91eb7-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="91eb7-129">RELATED LINKS</span></span>

