---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 55a3a45cf22dd6558a9728a254531a0e01627e20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450644"
---
# <span data-ttu-id="60aad-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="60aad-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="60aad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60aad-102">SYNOPSIS</span></span>
<span data-ttu-id="60aad-103">在磁片更新物件上設定圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="60aad-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60aad-104">句法</span><span class="sxs-lookup"><span data-stu-id="60aad-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <DiskUpdate> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60aad-105">說明</span><span class="sxs-lookup"><span data-stu-id="60aad-105">DESCRIPTION</span></span>
<span data-ttu-id="60aad-106">**AzureRmDiskUpdateImageReference** Cmdlet 會在磁片更新物件上設定 image 參照屬性。</span><span class="sxs-lookup"><span data-stu-id="60aad-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="60aad-107">示例</span><span class="sxs-lookup"><span data-stu-id="60aad-107">EXAMPLES</span></span>

### <span data-ttu-id="60aad-108">範例1</span><span class="sxs-lookup"><span data-stu-id="60aad-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="60aad-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="60aad-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="60aad-110">它也會設定 Windows OS 類型。</span><span class="sxs-lookup"><span data-stu-id="60aad-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="60aad-111">第二個命令會針對磁片更新物件設定影像識別碼和邏輯單元號碼0。</span><span class="sxs-lookup"><span data-stu-id="60aad-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="60aad-112">最後一個命令會取得磁片更新物件，並更新資源群組 "ResourceGroup01" 中名為「Disk01」的現有磁片。</span><span class="sxs-lookup"><span data-stu-id="60aad-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="60aad-113">參數</span><span class="sxs-lookup"><span data-stu-id="60aad-113">PARAMETERS</span></span>

### <span data-ttu-id="60aad-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="60aad-114">-DiskUpdate</span></span>
<span data-ttu-id="60aad-115">指定本機磁片更新物件。</span><span class="sxs-lookup"><span data-stu-id="60aad-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60aad-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="60aad-116">-Id</span></span>
<span data-ttu-id="60aad-117">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="60aad-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="60aad-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="60aad-118">-Lun</span></span>
<span data-ttu-id="60aad-119">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="60aad-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="60aad-120">-確認</span><span class="sxs-lookup"><span data-stu-id="60aad-120">-Confirm</span></span>
<span data-ttu-id="60aad-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60aad-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60aad-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60aad-122">-WhatIf</span></span>
<span data-ttu-id="60aad-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60aad-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60aad-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60aad-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60aad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60aad-125">CommonParameters</span></span>
<span data-ttu-id="60aad-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60aad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60aad-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60aad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60aad-128">輸入</span><span class="sxs-lookup"><span data-stu-id="60aad-128">INPUTS</span></span>

### <span data-ttu-id="60aad-129">DiskUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="60aad-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="60aad-130">System.object 系統為 Nullable "1 [（System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]）</span><span class="sxs-lookup"><span data-stu-id="60aad-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="60aad-131">輸出</span><span class="sxs-lookup"><span data-stu-id="60aad-131">OUTPUTS</span></span>

### <span data-ttu-id="60aad-132">DiskUpdate 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="60aad-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="60aad-133">筆記</span><span class="sxs-lookup"><span data-stu-id="60aad-133">NOTES</span></span>

## <span data-ttu-id="60aad-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="60aad-134">RELATED LINKS</span></span>

