---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 6746bc96f7c1a14d617f3147676556be7402b71c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916428"
---
# <span data-ttu-id="ba22b-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="ba22b-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="ba22b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ba22b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba22b-103">設定快照物件上的圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="ba22b-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="ba22b-104">語法</span><span class="sxs-lookup"><span data-stu-id="ba22b-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba22b-105">描述</span><span class="sxs-lookup"><span data-stu-id="ba22b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba22b-106">**Set-AzSnapshotImageReference** Cmdlet 會設定快照物件上的圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="ba22b-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="ba22b-107">例子</span><span class="sxs-lookup"><span data-stu-id="ba22b-107">EXAMPLES</span></span>

### <span data-ttu-id="ba22b-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ba22b-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="ba22b-109">第一個命令會建立大小為 10 GB 的儲存Premium_LRS快照物件。</span><span class="sxs-lookup"><span data-stu-id="ba22b-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ba22b-110">它也設定 Windows OS 類型。</span><span class="sxs-lookup"><span data-stu-id="ba22b-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="ba22b-111">第二個命令會設定快照物件的影像識別碼和邏輯單位數位 0。</span><span class="sxs-lookup"><span data-stu-id="ba22b-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="ba22b-112">最後一個命令會拍攝快照物件，在資源群組 "ResourceGroup01" 中建立名稱為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="ba22b-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ba22b-113">參數</span><span class="sxs-lookup"><span data-stu-id="ba22b-113">PARAMETERS</span></span>

### <span data-ttu-id="ba22b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba22b-114">-DefaultProfile</span></span>
<span data-ttu-id="ba22b-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba22b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba22b-116">-Id</span><span class="sxs-lookup"><span data-stu-id="ba22b-116">-Id</span></span>
<span data-ttu-id="ba22b-117">指定識別碼。</span><span class="sxs-lookup"><span data-stu-id="ba22b-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="ba22b-118">-四分位</span><span class="sxs-lookup"><span data-stu-id="ba22b-118">-Lun</span></span>
<span data-ttu-id="ba22b-119">指定在中 (單位) 。</span><span class="sxs-lookup"><span data-stu-id="ba22b-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba22b-120">-快照</span><span class="sxs-lookup"><span data-stu-id="ba22b-120">-Snapshot</span></span>
<span data-ttu-id="ba22b-121">指定本地快照物件。</span><span class="sxs-lookup"><span data-stu-id="ba22b-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba22b-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ba22b-122">-Confirm</span></span>
<span data-ttu-id="ba22b-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ba22b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba22b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba22b-124">-WhatIf</span></span>
<span data-ttu-id="ba22b-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba22b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba22b-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba22b-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba22b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba22b-127">CommonParameters</span></span>
<span data-ttu-id="ba22b-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ba22b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba22b-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba22b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba22b-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ba22b-130">INPUTS</span></span>

### <span data-ttu-id="ba22b-131">Microsoft.Azure.Commands.Compute.Automation.models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ba22b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="ba22b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ba22b-132">System.String</span></span>

### <span data-ttu-id="ba22b-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ba22b-133">System.Int32</span></span>

## <span data-ttu-id="ba22b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="ba22b-134">OUTPUTS</span></span>

### <span data-ttu-id="ba22b-135">Microsoft.Azure.Commands.Compute.Automation.models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="ba22b-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="ba22b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ba22b-136">NOTES</span></span>

## <span data-ttu-id="ba22b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba22b-137">RELATED LINKS</span></span>
