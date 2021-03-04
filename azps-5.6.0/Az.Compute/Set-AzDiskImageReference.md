---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: aed0113b229d41665effd7904d2de2357b4b5d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912041"
---
# <span data-ttu-id="03ab3-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="03ab3-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="03ab3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="03ab3-103">設定磁片物件上的圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="03ab3-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="03ab3-104">語法</span><span class="sxs-lookup"><span data-stu-id="03ab3-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03ab3-105">描述</span><span class="sxs-lookup"><span data-stu-id="03ab3-105">DESCRIPTION</span></span>
<span data-ttu-id="03ab3-106">**Set-Az以ImageReference** Cmdlet 設定磁片物件上的圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="03ab3-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="03ab3-107">例子</span><span class="sxs-lookup"><span data-stu-id="03ab3-107">EXAMPLES</span></span>

### <span data-ttu-id="03ab3-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="03ab3-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="03ab3-109">第一個命令會建立大小為 10 GB 的儲存Premium_LRS物件。</span><span class="sxs-lookup"><span data-stu-id="03ab3-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="03ab3-110">它也設定 Windows OS 類型。</span><span class="sxs-lookup"><span data-stu-id="03ab3-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="03ab3-111">第二個命令會設定磁片物件的影像識別碼和邏輯單位數位 0。</span><span class="sxs-lookup"><span data-stu-id="03ab3-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="03ab3-112">最後一個命令會取用磁片物件，在資源群組 'ResourceGroup01' 中建立名稱為 'Disk01' 的磁片。</span><span class="sxs-lookup"><span data-stu-id="03ab3-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="03ab3-113">參數</span><span class="sxs-lookup"><span data-stu-id="03ab3-113">PARAMETERS</span></span>

### <span data-ttu-id="03ab3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ab3-114">-DefaultProfile</span></span>
<span data-ttu-id="03ab3-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03ab3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ab3-116">-磁片</span><span class="sxs-lookup"><span data-stu-id="03ab3-116">-Disk</span></span>
<span data-ttu-id="03ab3-117">指定一個本地磁片物件。</span><span class="sxs-lookup"><span data-stu-id="03ab3-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="03ab3-118">-Id</span><span class="sxs-lookup"><span data-stu-id="03ab3-118">-Id</span></span>
<span data-ttu-id="03ab3-119">指定識別碼。</span><span class="sxs-lookup"><span data-stu-id="03ab3-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="03ab3-120">-四分位</span><span class="sxs-lookup"><span data-stu-id="03ab3-120">-Lun</span></span>
<span data-ttu-id="03ab3-121">指定在中 (單位) 。</span><span class="sxs-lookup"><span data-stu-id="03ab3-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="03ab3-122">-確認</span><span class="sxs-lookup"><span data-stu-id="03ab3-122">-Confirm</span></span>
<span data-ttu-id="03ab3-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="03ab3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03ab3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ab3-124">-WhatIf</span></span>
<span data-ttu-id="03ab3-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03ab3-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03ab3-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03ab3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03ab3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ab3-127">CommonParameters</span></span>
<span data-ttu-id="03ab3-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03ab3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ab3-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03ab3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ab3-130">輸入</span><span class="sxs-lookup"><span data-stu-id="03ab3-130">INPUTS</span></span>

### <span data-ttu-id="03ab3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="03ab3-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="03ab3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="03ab3-132">System.String</span></span>

### <span data-ttu-id="03ab3-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="03ab3-133">System.Int32</span></span>

## <span data-ttu-id="03ab3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="03ab3-134">OUTPUTS</span></span>

### <span data-ttu-id="03ab3-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="03ab3-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="03ab3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="03ab3-136">NOTES</span></span>

## <span data-ttu-id="03ab3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="03ab3-137">RELATED LINKS</span></span>
