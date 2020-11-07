---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 87786196e027597dc532bcaab2adfec4aa8c3892
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795933"
---
# <span data-ttu-id="13073-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="13073-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="13073-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13073-102">SYNOPSIS</span></span>
<span data-ttu-id="13073-103">在快照物件上設定圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="13073-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="13073-104">句法</span><span class="sxs-lookup"><span data-stu-id="13073-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13073-105">說明</span><span class="sxs-lookup"><span data-stu-id="13073-105">DESCRIPTION</span></span>
<span data-ttu-id="13073-106">**AzSnapshotImageReference** Cmdlet 會在快照物件上設定 image 參照屬性。</span><span class="sxs-lookup"><span data-stu-id="13073-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="13073-107">示例</span><span class="sxs-lookup"><span data-stu-id="13073-107">EXAMPLES</span></span>

### <span data-ttu-id="13073-108">範例1</span><span class="sxs-lookup"><span data-stu-id="13073-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="13073-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="13073-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="13073-110">它也會設定 Windows OS 類型。</span><span class="sxs-lookup"><span data-stu-id="13073-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="13073-111">第二個命令會設定快照 obejct 的影像識別碼和邏輯單元編號0。</span><span class="sxs-lookup"><span data-stu-id="13073-111">The second command sets the image ID and the logical unit number 0 for the snapshot obejct.</span></span>
<span data-ttu-id="13073-112">最後一個命令會採用快照物件，並會在資源群組 "ResourceGroup01" 中建立名為 "Snapshot01" 的快照。</span><span class="sxs-lookup"><span data-stu-id="13073-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="13073-113">參數</span><span class="sxs-lookup"><span data-stu-id="13073-113">PARAMETERS</span></span>

### <span data-ttu-id="13073-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13073-114">-DefaultProfile</span></span>
<span data-ttu-id="13073-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13073-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13073-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="13073-116">-Id</span></span>
<span data-ttu-id="13073-117">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="13073-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="13073-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="13073-118">-Lun</span></span>
<span data-ttu-id="13073-119">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="13073-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="13073-120">-快照</span><span class="sxs-lookup"><span data-stu-id="13073-120">-Snapshot</span></span>
<span data-ttu-id="13073-121">指定本機快照物件。</span><span class="sxs-lookup"><span data-stu-id="13073-121">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13073-122">-確認</span><span class="sxs-lookup"><span data-stu-id="13073-122">-Confirm</span></span>
<span data-ttu-id="13073-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13073-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13073-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13073-124">-WhatIf</span></span>
<span data-ttu-id="13073-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13073-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13073-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13073-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13073-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13073-127">CommonParameters</span></span>
<span data-ttu-id="13073-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13073-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13073-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13073-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13073-130">輸入</span><span class="sxs-lookup"><span data-stu-id="13073-130">INPUTS</span></span>

### <span data-ttu-id="13073-131">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="13073-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="13073-132">System.object 系統為 Nullable "1 [（System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]）</span><span class="sxs-lookup"><span data-stu-id="13073-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="13073-133">輸出</span><span class="sxs-lookup"><span data-stu-id="13073-133">OUTPUTS</span></span>

### <span data-ttu-id="13073-134">[Azure. 管理]-[計算] 模型. 快照</span><span class="sxs-lookup"><span data-stu-id="13073-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="13073-135">筆記</span><span class="sxs-lookup"><span data-stu-id="13073-135">NOTES</span></span>

## <span data-ttu-id="13073-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="13073-136">RELATED LINKS</span></span>

