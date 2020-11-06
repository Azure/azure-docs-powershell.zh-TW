---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: d035890f6478c0b7fd767f12b8f9a27d4f765837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611837"
---
# <span data-ttu-id="7d533-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7d533-101">Set-AzMediaService</span></span>

## <span data-ttu-id="7d533-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d533-102">SYNOPSIS</span></span>
<span data-ttu-id="7d533-103">修改現有媒體服務的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="7d533-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="7d533-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d533-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d533-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d533-105">DESCRIPTION</span></span>
<span data-ttu-id="7d533-106">**AzMediaService** Cmdlet 會修改現有媒體服務的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="7d533-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="7d533-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d533-107">EXAMPLES</span></span>

### <span data-ttu-id="7d533-108">範例1：修改現有的媒體服務</span><span class="sxs-lookup"><span data-stu-id="7d533-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="7d533-109">第一個命令會建立一系列標記，並將這些標記儲存在名為 $Tags 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7d533-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="7d533-110">這個第二個命令會使用 $Tags 變數中儲存的標籤，更新屬於名為 ResourceGroup123 之資源群組的名為 MediaService001 的媒體服務。</span><span class="sxs-lookup"><span data-stu-id="7d533-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="7d533-111">此命令也會使用儲存在 $StorageAccounts 變數中的儲存空間設定物件陣列。</span><span class="sxs-lookup"><span data-stu-id="7d533-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="7d533-112">參數</span><span class="sxs-lookup"><span data-stu-id="7d533-112">PARAMETERS</span></span>

### <span data-ttu-id="7d533-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7d533-113">-AccountName</span></span>
<span data-ttu-id="7d533-114">指定此 Cmdlet 修改的媒體服務名稱。</span><span class="sxs-lookup"><span data-stu-id="7d533-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d533-115">-DefaultProfile</span></span>
<span data-ttu-id="7d533-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7d533-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d533-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d533-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d533-118">指定包含媒體服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d533-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="7d533-119">-StorageAccounts</span></span>
<span data-ttu-id="7d533-120">指定此 Cmdlet 與媒體服務相關聯的儲存帳戶陣列。</span><span class="sxs-lookup"><span data-stu-id="7d533-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d533-121">-Tag</span></span>
<span data-ttu-id="7d533-122">與媒體帳戶相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="7d533-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-123">-確認</span><span class="sxs-lookup"><span data-stu-id="7d533-123">-Confirm</span></span>
<span data-ttu-id="7d533-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d533-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d533-125">-WhatIf</span></span>
<span data-ttu-id="7d533-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d533-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d533-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d533-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d533-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d533-128">CommonParameters</span></span>
<span data-ttu-id="7d533-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d533-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d533-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d533-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d533-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7d533-131">INPUTS</span></span>

### <span data-ttu-id="7d533-132">System.object</span><span class="sxs-lookup"><span data-stu-id="7d533-132">System.String</span></span>

### <span data-ttu-id="7d533-133">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7d533-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7d533-134">PSStorageAccount [] 的 []</span><span class="sxs-lookup"><span data-stu-id="7d533-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="7d533-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7d533-135">OUTPUTS</span></span>

### <span data-ttu-id="7d533-136">PSMediaService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7d533-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="7d533-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7d533-137">NOTES</span></span>

## <span data-ttu-id="7d533-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d533-138">RELATED LINKS</span></span>

[<span data-ttu-id="7d533-139">AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7d533-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="7d533-140">新-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7d533-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="7d533-141">移除-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7d533-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

