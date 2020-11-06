---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 98297d46416b23cd127e5ab5b65ce2fcfac38aa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447149"
---
# <span data-ttu-id="9407a-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="9407a-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="9407a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9407a-102">SYNOPSIS</span></span>
<span data-ttu-id="9407a-103">取得快照的屬性</span><span class="sxs-lookup"><span data-stu-id="9407a-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9407a-104">句法</span><span class="sxs-lookup"><span data-stu-id="9407a-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9407a-105">說明</span><span class="sxs-lookup"><span data-stu-id="9407a-105">DESCRIPTION</span></span>
<span data-ttu-id="9407a-106">**AzureRmSnapshot** Cmdlet 會取得快照的屬性。</span><span class="sxs-lookup"><span data-stu-id="9407a-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="9407a-107">示例</span><span class="sxs-lookup"><span data-stu-id="9407a-107">EXAMPLES</span></span>

### <span data-ttu-id="9407a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9407a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="9407a-109">這個命令會取得訂閱所有快照的屬性。</span><span class="sxs-lookup"><span data-stu-id="9407a-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="9407a-110">範例2</span><span class="sxs-lookup"><span data-stu-id="9407a-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="9407a-111">這個命令會取得名為 "ResourceGroupName1" 的資源群組中所有快照的屬性</span><span class="sxs-lookup"><span data-stu-id="9407a-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="9407a-112">範例3</span><span class="sxs-lookup"><span data-stu-id="9407a-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="9407a-113">這個命令會取得名為 "ResourceGroupName1" 的資源群組中名為 "SnapshotName1" 的快照屬性</span><span class="sxs-lookup"><span data-stu-id="9407a-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="9407a-114">參數</span><span class="sxs-lookup"><span data-stu-id="9407a-114">PARAMETERS</span></span>

### <span data-ttu-id="9407a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9407a-115">-DefaultProfile</span></span>
<span data-ttu-id="9407a-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9407a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9407a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9407a-117">-ResourceGroupName</span></span>
<span data-ttu-id="9407a-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9407a-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9407a-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9407a-119">-SnapshotName</span></span>
<span data-ttu-id="9407a-120">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="9407a-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9407a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9407a-121">CommonParameters</span></span>
<span data-ttu-id="9407a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9407a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9407a-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9407a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9407a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9407a-124">INPUTS</span></span>

### <span data-ttu-id="9407a-125">System.object</span><span class="sxs-lookup"><span data-stu-id="9407a-125">System.String</span></span>

## <span data-ttu-id="9407a-126">輸出</span><span class="sxs-lookup"><span data-stu-id="9407a-126">OUTPUTS</span></span>

### <span data-ttu-id="9407a-127">System.object</span><span class="sxs-lookup"><span data-stu-id="9407a-127">System.Object</span></span>

## <span data-ttu-id="9407a-128">筆記</span><span class="sxs-lookup"><span data-stu-id="9407a-128">NOTES</span></span>

## <span data-ttu-id="9407a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="9407a-129">RELATED LINKS</span></span>

