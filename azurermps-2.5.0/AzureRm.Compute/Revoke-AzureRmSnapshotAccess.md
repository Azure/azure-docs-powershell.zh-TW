---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermsnapshotaccess
schema: 2.0.0
ms.openlocfilehash: bbde391c56d4b50320f15441b75b93d125771ccb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802565"
---
# <span data-ttu-id="e4219-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="e4219-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="e4219-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4219-102">SYNOPSIS</span></span>
<span data-ttu-id="e4219-103">吊銷快照存取權。</span><span class="sxs-lookup"><span data-stu-id="e4219-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4219-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4219-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4219-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4219-105">DESCRIPTION</span></span>
<span data-ttu-id="e4219-106">**Revoke AzureRmSnapshotAccess** Cmdlet 會吊銷快照的存取權。</span><span class="sxs-lookup"><span data-stu-id="e4219-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="e4219-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4219-107">EXAMPLES</span></span>

### <span data-ttu-id="e4219-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e4219-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="e4219-109">廢除名為「ResourceGroup01」的資源群組中名為「Snapshot01」的快照存取權</span><span class="sxs-lookup"><span data-stu-id="e4219-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="e4219-110">參數</span><span class="sxs-lookup"><span data-stu-id="e4219-110">PARAMETERS</span></span>

### <span data-ttu-id="e4219-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4219-111">-AsJob</span></span>
<span data-ttu-id="e4219-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e4219-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4219-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4219-113">-DefaultProfile</span></span>
<span data-ttu-id="e4219-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4219-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4219-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4219-115">-ResourceGroupName</span></span>
<span data-ttu-id="e4219-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4219-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e4219-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="e4219-117">-SnapshotName</span></span>
<span data-ttu-id="e4219-118">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4219-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="e4219-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e4219-119">-Confirm</span></span>
<span data-ttu-id="e4219-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e4219-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4219-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4219-121">-WhatIf</span></span>
<span data-ttu-id="e4219-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e4219-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4219-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e4219-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4219-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4219-124">CommonParameters</span></span>
<span data-ttu-id="e4219-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4219-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4219-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4219-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4219-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e4219-127">INPUTS</span></span>

### <span data-ttu-id="e4219-128">System.object</span><span class="sxs-lookup"><span data-stu-id="e4219-128">System.String</span></span>

## <span data-ttu-id="e4219-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e4219-129">OUTPUTS</span></span>

### <span data-ttu-id="e4219-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e4219-130">System.Object</span></span>

## <span data-ttu-id="e4219-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e4219-131">NOTES</span></span>

## <span data-ttu-id="e4219-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4219-132">RELATED LINKS</span></span>

