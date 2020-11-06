---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: e111de4f6eb168afdd7b16d4d0ee0297d44fb149
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451744"
---
# <span data-ttu-id="0047a-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="0047a-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="0047a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0047a-102">SYNOPSIS</span></span>
<span data-ttu-id="0047a-103">在磁片物件上設定圖像參照屬性。</span><span class="sxs-lookup"><span data-stu-id="0047a-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0047a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0047a-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0047a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0047a-105">DESCRIPTION</span></span>
<span data-ttu-id="0047a-106">**AzureRmDiskImageReference** Cmdlet 會在磁片物件上設定 image 參照屬性。</span><span class="sxs-lookup"><span data-stu-id="0047a-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="0047a-107">示例</span><span class="sxs-lookup"><span data-stu-id="0047a-107">EXAMPLES</span></span>

### <span data-ttu-id="0047a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0047a-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="0047a-109">第一個命令會在 Premium_LRS 儲存帳戶類型中，建立一個大小為10GB 的本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="0047a-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="0047a-110">它也會設定 Windows OS 類型。</span><span class="sxs-lookup"><span data-stu-id="0047a-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="0047a-111">第二個命令會為磁片物件設定影像識別碼和邏輯單位數位0。</span><span class="sxs-lookup"><span data-stu-id="0047a-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="0047a-112">最後一個命令會取得磁片物件，並在 [資源] 群組的 [ResourceGroup01] 中建立名為 "Disk01" 的磁片。</span><span class="sxs-lookup"><span data-stu-id="0047a-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0047a-113">參數</span><span class="sxs-lookup"><span data-stu-id="0047a-113">PARAMETERS</span></span>

### <span data-ttu-id="0047a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0047a-114">-DefaultProfile</span></span>
<span data-ttu-id="0047a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0047a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0047a-116">-磁片</span><span class="sxs-lookup"><span data-stu-id="0047a-116">-Disk</span></span>
<span data-ttu-id="0047a-117">指定本機磁片物件。</span><span class="sxs-lookup"><span data-stu-id="0047a-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="0047a-118">-識別碼</span><span class="sxs-lookup"><span data-stu-id="0047a-118">-Id</span></span>
<span data-ttu-id="0047a-119">指定 ID。</span><span class="sxs-lookup"><span data-stu-id="0047a-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="0047a-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="0047a-120">-Lun</span></span>
<span data-ttu-id="0047a-121">指定邏輯單位編號 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="0047a-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0047a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="0047a-122">-Confirm</span></span>
<span data-ttu-id="0047a-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0047a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0047a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0047a-124">-WhatIf</span></span>
<span data-ttu-id="0047a-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0047a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0047a-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0047a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0047a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0047a-127">CommonParameters</span></span>
<span data-ttu-id="0047a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0047a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0047a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0047a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0047a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="0047a-130">INPUTS</span></span>

### <span data-ttu-id="0047a-131">[Azure. 管理]. 磁片</span><span class="sxs-lookup"><span data-stu-id="0047a-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="0047a-132">System.object 系統為 Nullable "1 [（System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]）</span><span class="sxs-lookup"><span data-stu-id="0047a-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0047a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0047a-133">OUTPUTS</span></span>

### <span data-ttu-id="0047a-134">[Azure. 管理]. 磁片</span><span class="sxs-lookup"><span data-stu-id="0047a-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="0047a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0047a-135">NOTES</span></span>

## <span data-ttu-id="0047a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0047a-136">RELATED LINKS</span></span>

