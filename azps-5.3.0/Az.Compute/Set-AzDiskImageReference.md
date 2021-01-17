---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 78a6c3bf85fae4fab9c5b9a06c366760b55804fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449715"
---
# <span data-ttu-id="48d10-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="48d10-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="48d10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48d10-102">SYNOPSIS</span></span>
<span data-ttu-id="48d10-103">在磁片物件上設定圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="48d10-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="48d10-104">句法</span><span class="sxs-lookup"><span data-stu-id="48d10-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48d10-105">說明</span><span class="sxs-lookup"><span data-stu-id="48d10-105">DESCRIPTION</span></span>
<span data-ttu-id="48d10-106">**AzDiskImageReference** Cmdlet 會在磁片物件上設定 image 參照屬性。</span><span class="sxs-lookup"><span data-stu-id="48d10-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="48d10-107">示例</span><span class="sxs-lookup"><span data-stu-id="48d10-107">EXAMPLES</span></span>

### <span data-ttu-id="48d10-108">範例1</span><span class="sxs-lookup"><span data-stu-id="48d10-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="48d10-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="48d10-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="48d10-110">它也會設定 Windows OS 類型。</span><span class="sxs-lookup"><span data-stu-id="48d10-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="48d10-111">第二個命令會為磁片物件設定影像識別碼和邏輯單位數位0。</span><span class="sxs-lookup"><span data-stu-id="48d10-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="48d10-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="48d10-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="48d10-113">參數</span><span class="sxs-lookup"><span data-stu-id="48d10-113">PARAMETERS</span></span>

### <span data-ttu-id="48d10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d10-114">-DefaultProfile</span></span>
<span data-ttu-id="48d10-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48d10-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48d10-116">-磁片</span><span class="sxs-lookup"><span data-stu-id="48d10-116">-Disk</span></span>
<span data-ttu-id="48d10-117">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="48d10-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48d10-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="48d10-118">-Id</span></span>
<span data-ttu-id="48d10-119">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="48d10-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="48d10-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="48d10-120">-Lun</span></span>
<span data-ttu-id="48d10-121">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="48d10-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="48d10-122">-確認</span><span class="sxs-lookup"><span data-stu-id="48d10-122">-Confirm</span></span>
<span data-ttu-id="48d10-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48d10-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48d10-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48d10-124">-WhatIf</span></span>
<span data-ttu-id="48d10-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48d10-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48d10-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48d10-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48d10-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d10-127">CommonParameters</span></span>
<span data-ttu-id="48d10-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48d10-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d10-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48d10-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d10-130">輸入</span><span class="sxs-lookup"><span data-stu-id="48d10-130">INPUTS</span></span>

### <span data-ttu-id="48d10-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="48d10-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="48d10-132">System.object</span><span class="sxs-lookup"><span data-stu-id="48d10-132">System.String</span></span>

### <span data-ttu-id="48d10-133">System.object</span><span class="sxs-lookup"><span data-stu-id="48d10-133">System.Int32</span></span>

## <span data-ttu-id="48d10-134">輸出</span><span class="sxs-lookup"><span data-stu-id="48d10-134">OUTPUTS</span></span>

### <span data-ttu-id="48d10-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="48d10-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="48d10-136">筆記</span><span class="sxs-lookup"><span data-stu-id="48d10-136">NOTES</span></span>

## <span data-ttu-id="48d10-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="48d10-137">RELATED LINKS</span></span>
