---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: cf63923b278f009cb676c79642882e64e6b8e303
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801718"
---
# <span data-ttu-id="81d07-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="81d07-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="81d07-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81d07-102">SYNOPSIS</span></span>
<span data-ttu-id="81d07-103">移除快照。</span><span class="sxs-lookup"><span data-stu-id="81d07-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81d07-104">句法</span><span class="sxs-lookup"><span data-stu-id="81d07-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81d07-105">說明</span><span class="sxs-lookup"><span data-stu-id="81d07-105">DESCRIPTION</span></span>
<span data-ttu-id="81d07-106">**AzureRmSnapshot** Cmdlet 會移除快照。</span><span class="sxs-lookup"><span data-stu-id="81d07-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="81d07-107">示例</span><span class="sxs-lookup"><span data-stu-id="81d07-107">EXAMPLES</span></span>

### <span data-ttu-id="81d07-108">範例1</span><span class="sxs-lookup"><span data-stu-id="81d07-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="81d07-109">這個命令會移除 [資源] 群組 "ResourceGroup01" 中名為「Snapshot01」的快照。</span><span class="sxs-lookup"><span data-stu-id="81d07-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="81d07-110">參數</span><span class="sxs-lookup"><span data-stu-id="81d07-110">PARAMETERS</span></span>

### <span data-ttu-id="81d07-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81d07-111">-AsJob</span></span>
<span data-ttu-id="81d07-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="81d07-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="81d07-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d07-113">-DefaultProfile</span></span>
<span data-ttu-id="81d07-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81d07-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d07-115">-Force</span><span class="sxs-lookup"><span data-stu-id="81d07-115">-Force</span></span>
<span data-ttu-id="81d07-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="81d07-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81d07-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d07-117">-ResourceGroupName</span></span>
<span data-ttu-id="81d07-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="81d07-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="81d07-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="81d07-119">-SnapshotName</span></span>
<span data-ttu-id="81d07-120">指定快照的名稱。</span><span class="sxs-lookup"><span data-stu-id="81d07-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="81d07-121">-確認</span><span class="sxs-lookup"><span data-stu-id="81d07-121">-Confirm</span></span>
<span data-ttu-id="81d07-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81d07-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d07-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d07-123">-WhatIf</span></span>
<span data-ttu-id="81d07-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81d07-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d07-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81d07-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d07-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d07-126">CommonParameters</span></span>
<span data-ttu-id="81d07-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81d07-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d07-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81d07-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d07-129">輸入</span><span class="sxs-lookup"><span data-stu-id="81d07-129">INPUTS</span></span>

### <span data-ttu-id="81d07-130">System.object</span><span class="sxs-lookup"><span data-stu-id="81d07-130">System.String</span></span>

## <span data-ttu-id="81d07-131">輸出</span><span class="sxs-lookup"><span data-stu-id="81d07-131">OUTPUTS</span></span>

### <span data-ttu-id="81d07-132">System.object</span><span class="sxs-lookup"><span data-stu-id="81d07-132">System.Object</span></span>

## <span data-ttu-id="81d07-133">筆記</span><span class="sxs-lookup"><span data-stu-id="81d07-133">NOTES</span></span>

## <span data-ttu-id="81d07-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="81d07-134">RELATED LINKS</span></span>

