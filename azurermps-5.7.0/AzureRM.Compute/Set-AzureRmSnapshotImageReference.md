---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: 262184f82aa169b5e76d3b875d0e3ba27db4da38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444712"
---
# <span data-ttu-id="a36b7-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="a36b7-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="a36b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a36b7-102">SYNOPSIS</span></span>
<span data-ttu-id="a36b7-103">在快照物件上設定圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="a36b7-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a36b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="a36b7-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <Snapshot> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a36b7-105">說明</span><span class="sxs-lookup"><span data-stu-id="a36b7-105">DESCRIPTION</span></span>
<span data-ttu-id="a36b7-106">**AzureRmSnapshotImageReference** Cmdlet 會在快照物件上設定 image 參照屬性。</span><span class="sxs-lookup"><span data-stu-id="a36b7-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="a36b7-107">示例</span><span class="sxs-lookup"><span data-stu-id="a36b7-107">EXAMPLES</span></span>

### <span data-ttu-id="a36b7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a36b7-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="a36b7-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="a36b7-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a36b7-110">它也會設定 Windows OS 類型。</span><span class="sxs-lookup"><span data-stu-id="a36b7-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="a36b7-111">第二個命令會為快照物件設定影像識別碼和邏輯單元號0。</span><span class="sxs-lookup"><span data-stu-id="a36b7-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="a36b7-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="a36b7-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a36b7-113">參數</span><span class="sxs-lookup"><span data-stu-id="a36b7-113">PARAMETERS</span></span>

### <span data-ttu-id="a36b7-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a36b7-114">-Id</span></span>
<span data-ttu-id="a36b7-115">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="a36b7-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="a36b7-116">-Lun</span><span class="sxs-lookup"><span data-stu-id="a36b7-116">-Lun</span></span>
<span data-ttu-id="a36b7-117">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="a36b7-117">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36b7-118">-快照</span><span class="sxs-lookup"><span data-stu-id="a36b7-118">-Snapshot</span></span>
<span data-ttu-id="a36b7-119">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="a36b7-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a36b7-120">-確認</span><span class="sxs-lookup"><span data-stu-id="a36b7-120">-Confirm</span></span>
<span data-ttu-id="a36b7-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a36b7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a36b7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a36b7-122">-WhatIf</span></span>
<span data-ttu-id="a36b7-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a36b7-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a36b7-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a36b7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a36b7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36b7-125">CommonParameters</span></span>
<span data-ttu-id="a36b7-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a36b7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36b7-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a36b7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36b7-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a36b7-128">INPUTS</span></span>

### <span data-ttu-id="a36b7-129">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="a36b7-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="a36b7-130">System.object 系統為 Nullable "1 [（System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]）</span><span class="sxs-lookup"><span data-stu-id="a36b7-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="a36b7-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a36b7-131">OUTPUTS</span></span>

### <span data-ttu-id="a36b7-132">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="a36b7-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="a36b7-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a36b7-133">NOTES</span></span>

## <span data-ttu-id="a36b7-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a36b7-134">RELATED LINKS</span></span>

