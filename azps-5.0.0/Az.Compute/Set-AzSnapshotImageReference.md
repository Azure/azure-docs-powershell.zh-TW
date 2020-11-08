---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138943"
---
# <span data-ttu-id="a61ea-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="a61ea-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="a61ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a61ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a61ea-103">在快照物件上設定圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="a61ea-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="a61ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="a61ea-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a61ea-105">說明</span><span class="sxs-lookup"><span data-stu-id="a61ea-105">DESCRIPTION</span></span>
<span data-ttu-id="a61ea-106">**AzSnapshotImageReference** Cmdlet 會在快照物件上設定 image 參照屬性。</span><span class="sxs-lookup"><span data-stu-id="a61ea-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="a61ea-107">示例</span><span class="sxs-lookup"><span data-stu-id="a61ea-107">EXAMPLES</span></span>

### <span data-ttu-id="a61ea-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a61ea-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="a61ea-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="a61ea-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="a61ea-110">它也會設定 Windows OS 類型。</span><span class="sxs-lookup"><span data-stu-id="a61ea-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="a61ea-111">第二個命令會為快照物件設定影像識別碼和邏輯單元號0。</span><span class="sxs-lookup"><span data-stu-id="a61ea-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="a61ea-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="a61ea-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="a61ea-113">參數</span><span class="sxs-lookup"><span data-stu-id="a61ea-113">PARAMETERS</span></span>

### <span data-ttu-id="a61ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a61ea-114">-DefaultProfile</span></span>
<span data-ttu-id="a61ea-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a61ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a61ea-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="a61ea-116">-Id</span></span>
<span data-ttu-id="a61ea-117">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="a61ea-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="a61ea-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="a61ea-118">-Lun</span></span>
<span data-ttu-id="a61ea-119">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="a61ea-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="a61ea-120">-快照</span><span class="sxs-lookup"><span data-stu-id="a61ea-120">-Snapshot</span></span>
<span data-ttu-id="a61ea-121">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="a61ea-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="a61ea-122">-確認</span><span class="sxs-lookup"><span data-stu-id="a61ea-122">-Confirm</span></span>
<span data-ttu-id="a61ea-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a61ea-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a61ea-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a61ea-124">-WhatIf</span></span>
<span data-ttu-id="a61ea-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a61ea-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a61ea-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a61ea-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a61ea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61ea-127">CommonParameters</span></span>
<span data-ttu-id="a61ea-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a61ea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61ea-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a61ea-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61ea-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a61ea-130">INPUTS</span></span>

### <span data-ttu-id="a61ea-131">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a61ea-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="a61ea-132">System.object</span><span class="sxs-lookup"><span data-stu-id="a61ea-132">System.String</span></span>

### <span data-ttu-id="a61ea-133">System.object</span><span class="sxs-lookup"><span data-stu-id="a61ea-133">System.Int32</span></span>

## <span data-ttu-id="a61ea-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a61ea-134">OUTPUTS</span></span>

### <span data-ttu-id="a61ea-135">PSSnapshot 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a61ea-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="a61ea-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a61ea-136">NOTES</span></span>

## <span data-ttu-id="a61ea-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a61ea-137">RELATED LINKS</span></span>